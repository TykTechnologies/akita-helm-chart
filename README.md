# What is Akita

[Akita](https://www.akitasoftware.com/) is a tool that generate Open Api Specification (OAS) by observing your traffic.

### Akita Helm Chart

This repo is an Akita helm chart that you can install in your kubernetes cluster and akita will start producing OAS for your.

### How To use this helm chart

[Helm](https://helm.sh) Must be installed to use this chart.Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

`helm repo add <alias> https://tyktechnologies.github.io/akita-helm-chart`

For example if you choose `akita-online` as your alias you would write something like:
`helm repo add akita-online https://tyktechnologies.github.io/akita-helm-chart`

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
<alias>` to see the charts.

#### How To Install the chart into your cluster.
For this chart to work the following values are required:
1. *project* - This is the akita project you want to send the data into.You can create the project name from the [akita console](https://app.akita.software/).
2. *apiKeyId* - It has to be base64 encoded.You can get it from the [akita console](https://app.akita.software/).
3. *apiKeySecret* - It has to be base64 encoded.You can get it from the [akita console](https://app.akita.software/).

**Optional Values**
1. port -This is the port whose traffic you want to monitor.For example if your app listens on port 9007 you will pass 9007 as the port.If not provided it will default to port 9007

To install the akita-helm-chart chart into your cluster run:
`helm install <release name> <alias>/akita-helm-chart --set apiKeyId=<base 64 enconded apiKeyId> --set apiKeySecret=<base 64 enconded apiKeySecret> --set project=<the-akita-project>`

After the installation akita will start creating the OAS for you!!

#### To uninstall the chart from your cluster:
`helm delete <release name>`