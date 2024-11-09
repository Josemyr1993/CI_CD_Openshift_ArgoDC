# CI_CD_Openshift_ArgoDC
<img src="https://github.com/Josemyr1993/CI_CD_Openshift_ArgoDC/blob/main/Animation.gif" heigh="500" width="700">


On this project, we use online Red Hat Developer Sandbox, it's a free environment for PoC configurations - [Openshift Sand Box URL](https://developers.redhat.com/developer-sandbox)

<h3>Objective</h3>

To show how to create projects into Kubernetes-native pipelines to do our CI/CD to ficilitate deploy services and applications using [ArgoCD](https://argo-cd.readthedocs.io/en/stable/) as CD tool;

<h3>Explaining th developer workflow above</h3>

1. A developer implements a change request.
2. Once The developer commits the changes to git, an integration pipeline is triggered.
3. This pipeline compiles the code, runs all automated tests, and creates and pushes the image.
4. Finally, the pipeline automatically installs the application on the test system. With GitOps, the developer wokflow looks somewhat different.

<h3> GitOps ArgoCD Process workflow </h3>

1. A developer implements a change request.
2. Once the developer commits the change to Git, an integration pipeline is triggered.
3. This pipeline compiles the code, runs all automated tests, and creates and pushes the image.
4. The pipeline automatically updates the configuration file's directory in the Git repository to reflect the changes.
5. The CD tool (ArgoCD) sees a new desired state in Git, which is then synchronized to the kubernetes environment.


<h3>Project Structure</h3>

```
$ tree
└── config
    ├── base
    │   ├── config-map.yaml
    │   ├── deployment.yaml
    │   ├── kustomization.yaml
    │   ├── route.yaml
    │   └── service.yaml
    └── overlays
        ├── dev
        │   └── kustomization.yaml
        ├── prod
        │   └── kustomization.yaml
        └── stage
            ├── apply-health-checks.yaml
            ├── change-env-value.yaml
            └── kustomization.yaml

```

<h1>References</h1>

- Getting-GitOps-ebook
