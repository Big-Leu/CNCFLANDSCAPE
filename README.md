## Application Definition & Image Build

### Helm Overview

**Helm** is a tool for managing Kubernetes applications using **Charts**—pre-configured packages of Kubernetes resources.

#### Key Features
- **Discover & Deploy:** Use Helm Charts to easily find and deploy software in Kubernetes.
- **Share Applications:** Distribute your Kubernetes applications as Helm Charts.
- **Reproducible Builds:** Ensure consistent builds of your applications with Helm.
- **Manifest Management:** Simplify the management of Kubernetes manifest files.
- **Release Management:** Manage application releases, including rollbacks and upgrades.

#### Components
- **Charts:** Helm packages that include:
  - `Chart.yaml`: Describes the package.
  - Templates: Contain Kubernetes manifest files.
- **Chart Repositories:** Store Charts locally or fetch from remote repositories.

#### Usage
Helm operates in various environments (local, CI/CD, etc.) and interacts directly with the Kubernetes API to deploy and manage applications.


### Artifact Hub

[Artifact Hub](https://artifacthub.io) is a web-based application that enables finding, installing, and publishing packages and configurations for Cloud Native packages.

Discovering artifacts to use with CNCF projects can be difficult. If every CNCF project that needs to share artifacts creates its own Hub this creates a fair amount of repeat work for each project and a fractured experience for those trying to find the artifacts to consume. The Artifact Hub attempts to solve that by providing a single experience for consumers that any CNCF project can leverage.

At the moment, the following artifacts kinds are supported *(with plans to support more projects to follow)*:

- [Argo templates](https://argoproj.github.io/argo-workflows/)
- [Backstage plugins](https://backstage.io)
- [Containers images](https://opencontainers.org)
- [CoreDNS plugins](https://coredns.io/)
- [Falco configurations](https://falco.org/)
- [Gatekeeper policies](https://open-policy-agent.github.io/gatekeeper/website/docs/)
- [Headlamp plugins](https://headlamp.dev)
- [Helm charts](https://helm.sh/)
- [Helm plugins](https://helm.sh/docs/topics/plugins/)
- [Inspektor Gadgets](https://www.inspektor-gadget.io)
- [KCL modules](https://kcl-lang.io)
- [KEDA scalers](https://keda.sh/)
- [Keptn integrations](https://keptn.sh)
- [Knative client plugins](https://knative.dev)
- [KubeArmor policies](https://kubearmor.io)
- [Kubectl plugins (Krew)](https://krew.sigs.k8s.io/)
- [Kubewarden policies](https://www.kubewarden.io)
- [Kyverno policies](https://kyverno.io)
- [Meshery designs](https://meshery.io)
- [OLM operators](https://github.com/operator-framework)
- [OpenCost plugins](https://www.opencost.io)
- [Open Policy Agent (OPA) policies](https://www.openpolicyagent.org/)
- [Tekton tasks, pipelines and stepactions](https://tekton.dev/)
- [Tinkerbell actions](https://tinkerbell.org/)


### [Backstage](https://backstage.io)


## What is Backstage?

[Backstage](https://backstage.io/) is an open source framework for building developer portals. Powered by a centralized software catalog, Backstage restores order to your microservices and infrastructure and enables your product teams to ship high-quality code quickly without compromising autonomy.

Backstage unifies all your infrastructure tooling, services, and documentation to create a streamlined development environment from end to end.

### pack - Buildpack CLI


`pack` makes it easy for...
- [**App Developers**][app-dev] to use buildpacks to convert code into runnable images.
- [**Buildpack Authors**][bp-author] to develop and package buildpacks for distribution.
- [**Operators**][operator] to package buildpacks for distribution and maintain applications.

### Dapr


Dapr is a portable, serverless, event-driven runtime that makes it easy for developers to build resilient, stateless and stateful microservices that run on the cloud and edge and embraces the diversity of languages and developer frameworks.

Dapr codifies the *best practices* for building microservice applications into open, independent, building blocks that enable you to build portable applications with the language and framework of your choice. Each building block is independent and you can use one, some, or all of them in your application.


## Goals

- Enable developers using *any* language or framework to write distributed applications
- Solve the hard problems developers face building microservice applications by providing best practice building blocks
- Be community driven, open and vendor neutral
- Gain new contributors
- Provide consistency and portability through open APIs
- Be platform agnostic across cloud and edge
- Embrace extensibility and provide pluggable components without vendor lock-in
- Enable IoT and edge scenarios by being highly performant and lightweight
- Be incrementally adoptable from existing code, with no runtime dependency

## How it works

Dapr injects a side-car (container or process) to each compute unit. The side-car interacts with event triggers and communicates with the compute unit via standard HTTP or gRPC protocols. This enables Dapr to support all existing and future programming languages without requiring you to import frameworks or libraries.

Dapr offers built-in state management, reliable messaging (at least once delivery), triggers and bindings through standard HTTP verbs or gRPC interfaces. This allows you to write stateless, stateful and actor-like services following the same programming paradigm. You can freely choose consistency model, threading model and message delivery patterns.

Dapr runs natively on Kubernetes, as a self hosted binary on your machine, on an IoT device, or as a container that can be injected into any system, in the cloud or on-premises.

Dapr uses pluggable component state stores and message buses such as Redis as well as gRPC to offer a wide range of communication methods, including direct dapr-to-dapr using gRPC and async Pub-Sub with guaranteed delivery and at-least-once semantics.

## Kubevela
### Introduction

KubeVela is a modern application delivery platform that makes deploying and operating applications across today's hybrid, multi-cloud environments easier, faster and more reliable.



## Highlights

KubeVela practices the "render, orchestrate, deploy" workflow with below highlighted values added to existing ecosystem:

#### **Deployment as Code**

Declare your deployment plan as workflow, run it automatically with any CI/CD or GitOps system, extend or re-program the workflow steps with [CUE](https://cuelang.org/).
No ad-hoc scripts, no dirty glue code, just deploy. The deployment workflow in KubeVela is powered by [Open Application Model](https://oam.dev/).

#### **Built-in observability, multi-tenancy and security support**

Choose from the wide range of LDAP integrations we provided out-of-box, enjoy enhanced [multi-tenancy and multi-cluster authorization and authentication](https://kubevela.net/docs/platform-engineers/auth/advance),
pick and apply fine-grained RBAC modules and customize them as per your own supply chain requirements.
All delivery process has fully [automated observability dashboards](https://kubevela.net/docs/platform-engineers/operations/observability).

#### **Multi-cloud/hybrid-environments app delivery as first-class citizen**

Natively supports multi-cluster/hybrid-cloud scenarios such as progressive rollout across test/staging/production environments,
automatic canary, blue-green and continuous verification, rich placement strategy across clusters and clouds,
along with automated cloud environments provision.

#### **Lightweight but highly extensible architecture**

Minimize your control plane deployment with only one pod and 0.5c1g resources to handle thousands of application delivery.
Glue and orchestrate all your infrastructure capabilities as reusable modules with a highly extensible architecture
and share the large growing community [addons](https://kubevela.net/docs/reference/addons/overview).

## KubeVirt

**KubeVirt** is a virtual machine management add-on for Kubernetes.
The aim is to provide a common ground for virtualization solutions on top of
Kubernetes.

## Introduction

### Virtualization extension for Kubernetes

At its core, KubeVirt extends [Kubernetes][k8s] by adding
additional virtualization resource types (especially the `VM` type) through
[Kubernetes's Custom Resource Definitions API][crd].
By using this mechanism, the Kubernetes API can be used to manage these `VM`
resources alongside all other resources Kubernetes provides.

The resources themselves are not enough to launch virtual machines.
For this to happen the _functionality and business logic_ needs to be added to
the cluster. The functionality is not added to Kubernetes itself, but rather
added to a Kubernetes cluster by _running_ additional controllers and agents
on an existing cluster.

The necessary controllers and agents are provided by KubeVirt.

As of today KubeVirt can be used to declaratively

 * Create a predefined VM
 * Schedule a VM on a Kubernetes cluster
 * Launch a VM
 * Stop a VM
 * Delete a VM


## Operator Framework

### Overview

This project is a component of the [Operator Framework][of-home], an
open source toolkit to manage Kubernetes native applications, called
Operators, in an effective, automated, and scalable way. Read more in
the [introduction blog post][of-blog].

[Operators][operator-link] make it easy to manage complex stateful
applications on top of Kubernetes. However writing an Operator today can
be difficult because of challenges such as using low level APIs, writing
boilerplate, and a lack of modularity which leads to duplication.

The Operator SDK is a framework that uses the
[controller-runtime][controller-runtime] library to make writing
operators easier by providing:

- High level APIs and abstractions to write the operational logic more intuitively
- Tools for scaffolding and code generation to bootstrap a new project fast
- Extensions to cover common Operator use cases

# Continuous Integration & Delivery

# Argo CD - Declarative Continuous Delivery for Kubernetes

## What is Argo CD?

Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.


[![Argo CD Demo](https://img.youtube.com/vi/0WAm0y2vLIo/0.jpg)](https://youtu.be/0WAm0y2vLIo)

## Why Argo CD?

1. Application definitions, configurations, and environments should be declarative and version controlled.
1. Application deployment and lifecycle management should be automated, auditable, and easy to understand.

## Who uses Argo CD?

[Official Argo CD user list](USERS.md)

## Documentation

To learn more about Argo CD [go to the complete documentation](https://argo-cd.readthedocs.io/).
Check live demo at https://cd.apps.argoproj.io/.

## Flux version 2


Flux is a tool for keeping Kubernetes clusters in sync with sources of
configuration (like Git repositories and OCI artifacts),
and automating updates to configuration when there is new code to deploy.

Flux version 2 ("v2") is built from the ground up to use Kubernetes'
API extension system, and to integrate with Prometheus and other core
components of the Kubernetes ecosystem. In version 2, Flux supports
multi-tenancy and support for syncing an arbitrary number of Git
repositories, among other long-requested features.

Flux v2 is constructed with the [GitOps Toolkit](#gitops-toolkit), a
set of composable APIs and specialized tools for building Continuous
Delivery on top of Kubernetes.

Flux is a Cloud Native Computing Foundation ([CNCF](https://www.cncf.io/)) graduated project, used in
production by various [organisations](https://fluxcd.io/adopters) and [cloud providers](https://fluxcd.io/ecosystem).

# Keptn

This is the primary repository for
the Keptn software and documentation.
Keptn provides a “cloud-native” approach
for managing the application release lifecycle
metrics, observability, health checks,
with pre- and post-deployment evaluations and tasks.
It is an incubating project, under the umbrella of the
[Keptn Application Lifecycle working group](https://github.com/keptn/wg-app-lifecycle).

> **Note** Keptn was developed under the code name of
  "Keptn Lifecycle Toolkit" or "KLT" for short.
  The source code contains many vestiges of these names.

## Goals

Keptn provides Cloud Native teams with the following capabilities:

- Pre-requisite evaluation before deploying workloads and applications
- Checking the Application Health in a declarative (cloud-native) way
- Standardized way to run pre- and post-deployment tasks
- Provide out-of-the-box Observability
- Deployment lifecycle management


Keptn can be seen as a general purpose and declarative
[Level 3 operator](https://operatorframework.io/operator-capabilities/)
for your Application.
For this reason, Keptn is agnostic to deployment tools
that are used and works with any GitOps solution.

For more information about the core concepts of Keptn, see
our core concepts
[documentation section](https://keptn.sh/stable/docs/core-concepts/).

## Kruise

### Introduction

OpenKruise  (official site: [https://openkruise.io](https://openkruise.io)) is a CNCF([Cloud Native Computing Foundation](https://cncf.io/)) incubating project.
It consists of several controllers which extend and complement the [Kubernetes core controllers](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/) for workload and application management.

## Key Features

- **Advance Workloads**

  Advance Workloads can help you manage applications of stateless, stateful, daemon and job.

  They all support not only the basic features which are similar to the original Workloads in Kubernetes, but also more advanced abilities like **in-place update**, **configurable scale/upgrade strategies**, **parallel operations**.

  - [**CloneSet** for stateless applications](https://openkruise.io/docs/user-manuals/cloneset/)
  - [**Advanced StatefulSet** for stateful applications](https://openkruise.io/docs/user-manuals/advancedstatefulset)
  - [**Advanced DaemonSet** for daemon applications](https://openkruise.io/docs/user-manuals/advanceddaemonset)
  - [**BroadcastJob** for deploying jobs over specific nodes](https://openkruise.io/docs/user-manuals/broadcastjob)
  - [**AdvancedCronJob** for creating Job or BroadcastJob periodically](https://openkruise.io/docs/user-manuals/advancedcronjob)

- **Sidecar container Management**

  Kruise simplify sidecar injection and enable sidecar in-place update. Kruise also enhance the sidecar startup and termination control.

  - [**SidecarSet** for defining and upgrading your own sidecars](https://openkruise.io/docs/user-manuals/sidecarset)
  - [**Container Launch Priority** to control the container startup orders](https://openkruise.io/docs/user-manuals/containerlaunchpriority)
  - [**Sidecar Job Terminator** terminates sidecar containers for such job-type Pods when its main containers completed.](https://openkruise.io/docs/user-manuals/jobsidecarterminator)

- **Multi-domain Management**

  This can help you manage applications over nodes with multiple domains,
  such as different node pools, available zones, architectures(x86 & arm) or node types(kubelet & virtual kubelet).

  Here we provide two different ways:

  - [**WorkloadSpread** for bypass distributing pods in workloads](https://openkruise.io/docs/user-manuals/workloadspread)
  - [**UnitedDeployment**, a new workload to manage multiple sub-workloads](https://openkruise.io/docs/user-manuals/uniteddeployment)

- **Enhanced Operations**

  - [**ContainerRecreateRequest** provides a way to let users restart/recreate containers in a running pod](https://openkruise.io/docs/user-manuals/containerrecreaterequest)
  - [**ImagePullJob** pre-download images on specific nodes](https://openkruise.io/docs/user-manuals/imagepulljob)
  - [**ResourceDistribution** support Secret & ConfigMap resource distribution across namespaces](https://openkruise.io/docs/user-manuals/resourcedistribution)
  - [**PersistentPodState** is able to persistent states of the Pod, such as "IP Retention"](https://openkruise.io/docs/user-manuals/persistentpodstate)
  - [**PodProbeMarker** provides the ability to customize the Probe and return the result to the Pod](https://openkruise.io/docs/user-manuals/podprobemarker)

- **Application Protection**

  - [Protect Kubernetes resources and applications' availability from the cascading deletion](https://openkruise.io/docs/user-manuals/deletionprotection)
  - [**PodUnavailableBudget** for achieving the effect of preventing application disruption or SLA degradation](https://openkruise.io/docs/user-manuals/podunavailablebudget)