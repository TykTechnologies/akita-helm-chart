# What is Akita 

Akita is a tool that generate Open Api Specification (OAS) by observing your traffic.

# Akita Helm Chart

This repo is an  Akita helm chart that you can install on your kubernetes cluster.

# How To use this helm chart

 [Helm](https://helm.sh) Must be installed to use this charts.Please refer to
 Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

`helm repo add <alias> https://tyktechnologies.github.io/akita-helm-chart`

If you had already added this repo earlier, run `helm repo update` to retrieve
 the latest versions of the packages.  You can then run `helm search repo
 <alias>` to see the charts.

To install the akita-helm-charts chart  to you cluster run:
`helm install my-<chart-name> <alias>/<chart-name>`

To uninstall the chart:
`helm delete my-<chart-name>`

# Values You have to change in the Values.yaml