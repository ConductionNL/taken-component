# Taken Component / TC

Description
----
The Tasks Component offers the generic possibility to register tasks from one resource on another resource (for example Common Ground resources). This functionality is deliberately set up abstract. In the most common form, for example, an employee or user (resource) will have a task on a business or order (resource), but in abstract form a citizen (BRP resource) can also have a task or even applications or processes (as included in the PC) have a task. In this sense, the Tasks Component gives substance to tasks as well as the agenda calendar concept “todo” and the bpmn concept “task”. However, both the subject of the task and the performer of the task must be identifiable by a URL.

This means that there is automatic support for simple fulfillment flows, for example tasks could be assigned to a "User Group" and then picked up by a user in that group.

Memos are in principle seen as internal to the organization, and are emphatically not a communication channel with the customer (contact moments are available for this).

Additional Information
----

- [Contributing](CONTRIBUTING.md)
- [ChangeLogs](CHANGELOG.md)
- [RoadMap](ROADMAP.md)
- [Security](SECURITY.md)
- [Licence](LICENSE.md)


Installation
----
We differentiate between two way's of installing this component, a local installation as part of the provided developers toolkit or an [helm](https://helm.sh/) installation on an development or production environment. 

#### Local installation
First make sure you have [docker desktop](https://www.docker.com/products/docker-desktop) running on your computer. Then clone the repository to a directory on your local machine through a [git command](https://github.com/git-guides/git-clone) or [git kraken](https://www.gitkraken.com) (ui for git). If successful you can now navigate to the directory of your cloned repository in a command prompt and execute docker-compose up. 
```CLI
$ docker-compose up
```
This will build the docker image and run the used containers and when seeing the log from the php container: "NOTICE: ready to handle connections", u are ready to view the documentation at localhost on your preferred browser.

#### Instalation on Kubernetes or Haven
As a haven compliant commonground component this component is installable on kubernetes trough helm. The helm files can be found in the api/helm folder. For installing this component trough helm simply open your (still) favorite command line interface and run 
```CLI
$ helm install [name] ./api/helm --kubeconfig kubeconfig.yaml --namespace [name] --set settings.env=prod,settings.debug=0,settings.cache=1
```
For an in depth installation guide you can refer to the [installation guide](INSTALLATION.md), it also contains a short tutorial on getting your cluster ready to expose your installation to the world

Developers toolkit and technical information
----

We make our datamodels with the tool [modelio](https://www.modelio.org) which can be found along the OAS documentation and the postman collection in api/public/schema.
If you need development support we provide that through the [samenorganiseren slack channel](https://join.slack.com/t/samenorganiseren/shared_invite/zt-dex1d7sk-wy11sKYWCF0qQYjJHSMW5Q).

Couple of quick tips when you start developing
- If you haven't setup the component locally read the Installation part for setting up your local environment.
- You can find the other components on [Github](https://github.com/ConductionNL).
- Take a look at the [commonground componenten catalogus](https://componentencatalogus.commonground.nl/componenten?) to prevent development collitions. 
- Use [Commongroun.conduction.nl](https://commonground.conduction.nl/) for easy deployment of test environments to deploy your development to.
- For information on how to work with the component you can refer to the tutorial [here](TUTORIAL.md).
  

Contributing
----
First of al please read the [Contributing](CONTRIBUTING.md) guideline's ;)

But most imporantly, welcome! We strife to keep an active community at [commonground.nl](https://commonground.nl/), please drop by and tell is what you are thinking about so that we can help you along.


Credits
----

Information about the authors of this component can be found [here](AUTHORS.md)


Copyright © [Utrecht](https://www.utrecht.nl/) 2019
