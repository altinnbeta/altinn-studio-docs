---
title: Altinn Studio Apps - Deployment Architecture
linktitle: Altinn Studio Apps
description: Description of the deployment architecture for Altinn Studio Apps
tags: ["tjenester 3.0"]
weight: 100
---
{{% notice warning %}}
NOTE: Work in progress. Stuff will change
{{% /notice %}}

Altinn Studio Apps is the solution where all the services developed in Altinn Studio is deployed.
The following diagram shows the deploy architecture for Altinn Studio Apps

{{%excerpt%}}
<object data="/architecture/deployment/altinn-studio-apps/AltinnStudioApps_deployment_Architecture.svg" type="image/svg+xml" style="width: 100%;"></object>
{{% /excerpt%}}

### Service Containers
In the Altinn Studio Apps  solution each end user service will have a uniqe docker container managed 
by Kubernetes. Each set of service containers will be scaled based on the use of the service.
The service container will consist of the runtime application and service specific code and configuration.

### Routing
To be able to route traffic to the correct container, each container is tagged to a specific 
end user service. The routing mecahnism routes to the correct container based on the url 
containing the service parameter.

### Data services
The data services application is the application responsible exposing data related functionality 
to the service containers. This container will be scaled based on need.

### Platform integration
The platform integration is a new application hosted in the existing infrastructure. 
It exposes REST-APIs for Profile, Register, Authorization, Intermediary and Authentication. 
These are services not part of the Altinn Studio Platform (yet) and
everyone planning to run the Altinn Studio platform would need to implement their own components that support. 

### API Proxy
API Proxy is needed for controlling credentials and outbound firewall rules from the platform. 
This might be handled by the API Managment software. Needs Analyzis

### API Management
The platform requires API management software to handle SLA ++. Needs Analyzis



