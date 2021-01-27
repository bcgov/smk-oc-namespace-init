# Intro

<img src="https://lh3.googleusercontent.com/pw/ACtC-3cKoo1J7HQqfYbwBp9N0p5RaO78VGiM4448hg-Uu8lcHOnHFzHCwNrfTj98RtMVu6mrWxJiVyLlWEAZMdhWQ5A1Dp4K7M7tK-c9GpjpkO_Yz2uMfjW0nIkykjk04lmKXhuoeNmuJ1nbvUEsuIw6Z0konw=w1020-h574-no?authuser=0" width="500">

Helm chart used to init a net new openshift namespace where smk based apps will 
ultimately be deployed.  The chart creates objects that are re-used by all 
subsequent SMK based app deployments.

This repo follows the same pattern as the bcgov helm chart repo:
https://github.com/bcgov/helm-charts

# Contents

## smk-init 

This chart initializes a openshift namespace so that it contains the objects that are required
to support the smk github actions.  This only needs to be done once per namespace.

## smk-app-deploy

This is the chart that will get run by the [github actions](https://github.com/bcgov/smk-actions/tree/main/smk-deploy)
in each repository that it is enabled for.  It is set up to deploy SMK based apps where the directory structure
follows the layout described [here](https://github.com/bcgov/smk-actions/blob/main/docs/addBuildDeployFiles.md#details)

