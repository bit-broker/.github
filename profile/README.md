# Welcome to BitBroker

BitBroker is a policy-based, data sharing engine which enables you to securely share:

* The data segments you _permit_
* In ways which you _allow_
* With organisations that you _approve_

It's a complete, end-to-end data sharing solution, allowing you to __Share Your Data with Confidence__

If you are new to BitBroker, you should head over to our main website at [www.bit-broker.io](https://www.bit-broker.io/). There you can learn all about the project, what it does, how it works and how to leverage it for your own data sharing use cases. Amongst other things, you will find:

* A full set of interactive [demos](https://demo.bit-broker.io) which show a live working instance of BitBroker
* A clear and simple [getting started guide](https://www.bit-broker.io/docs/getting-started/), to help you deploy and operate your own BitBroker instance
* Full system and technical [documentation](https://www.bit-broker.io/docs/), detailing everything you need to know to leverage BitBroker
* Lots of [samples and example](https://www.bit-broker.io/docs/getting-started/demo/) so get you started on extracting value from BitBroker

Why not start by playing with the demo instance. Its just a few clicks aways and requires nothing but a browser and a few minutes of your time.

You can get timely updates and news by [following us on Twitter](https://twitter.com/broker_bit).

## Open Source

BitBroker is open source under the generous and permissive [Apache 2](https://github.com/bit-broker/.github/blob/main/LICENSE) license.

## Repositories

The following is a breakdown of the repositories you will find within this GitHub organisation.

Repo | Description
--- | ---
`bit-broker` | The main API based brokering engine
`portal` | The web-portal, wrapping all services within a UI
`website` | The public website at [www.bit-broker.io](https://www.bit-broker.io/)
`charts` | A full suite of [Kubernetes](https://kubernetes.io/) deployment charts and scripts
`auth-service` | An authorisation service used to guard access to APIs
`rate-service` | A rate limiting service used to policy based access controls

You will find more technical documentation is held within the readme structures of the repositories themselves. The [getting started guide](https://www.bit-broker.io/docs/getting-started/) is the best place to head to in order to get these components up and running in your own deployment space.

## Issues and Questions

If you have issues or questions about BitBroker, we would encourage you first to have a good root around the [public documentation](https://www.bit-broker.io/docs/). Here you should find the answer to the most frequent questions. We will improve this documentation whenever new questions arise.

If you don't find an answer to your question or issue, then please feel free to open a new issue on [this main organisation wide](https://github.com/bit-broker/.github/issues) repo. We endeavour to respond to all new issues in a prompt and timely manner. We might move your issue to one of the sub-repos if it more appropriately belongs there.

If you have a specific issue with one component which makes up BitBroker, then you should open an issue on that repository directly. But, please do search through the existing open issue first in order to minimise duplication and potentially save yourself time. If you find an open issue already, do add a note to it explaining your perspective and experiences.

__TODO__ - Should we introduce a better question channel like slack, teams or even email?

## Contributing to BitBroker

We welcome contributions from people on any or all of the repositories which make up the system.

### The Core Team

The current BitBroker core team is:

Member | Role
--- | ---
[Stephen Augustus](https://github.com/justaugustus) | admin
[Pete Rai](https://github.com/pete-rai) | admin
[James Walker](https://github.com/jgwalker) | maintainer
[Jean Diaconu](https://github.com/jadiaconu) | maintainer

Together this group forms the leadership of the BitBroker project. All key project decisions will be made by this group, which will meet on a regular basis. Please feel free to lobby any one of them in order to voice issues which you want addressed. Remember, the best approach is to first create an issue using the appropriate issue tracking mechanism listed earlier in this document.

All the decisions made by the leadership group will be documented clearly either in the project documentation or in response to specific issues raised in the issue tracking area.

### Project Governance

Given the early stage of the project, the project will operate in a de-facto "Benevolent Dictator" model, where the "dictator" is the small core BitBroker team outlined earlier in this document. This team has the final say on all major project decisions. Contributors who have issues, requests or suggestions are encouraged to contact any member of this team, who will then bring it to the attention of the others. The team commit to meet on a regular basis and to publish all their decisions in an open and transparent way.

The core team is committed to moving to a more community led approach for BitBroker in the future, when the project is more established and its goals and boundaries are better understood and defined.

### Code of Conduct

At this stage, we do not have an extensive formal Code of Conduct document. However we do have some basic requirements which we ask that contributors respect.

#### Expectations

The BitBroker team is committed to open and positive communication to promote an environment that ensures that all participants feel welcomed, respected and supported. We recognise that the GitHub community is diverse and that people have different backgrounds, experiences, and understandings of what constitutes offensive or inappropriate behaviour. We ask the all contributors apply common sense rules as to their own behaviour and think carefully about how their actions and communications might be perceived by other people.

The BitBroker team will not tolerate any behaviour which we deem to be offensive or inappropriate.

Examples of such behaviour are (but not limited too): Offensive comments related to personal traits or lifestyle choices and practices, sexual references or unwanted sexual attention, threats, intimidation, disruption, doxing, etc. Ultimately, the team reserves the right to decide what is-and-is-not acceptable behaviour.
Reporting

If you witness behaviour which you think is not appropriate, we encourage you to sensitively and respectfully dissuade the originator from such behaviour. If such behaviour continues, or is of a very serious nature, you should contact the BitBroker leadership team.

If you are the victim of behaviour which you feel is inappropriate or offensive, you should contact the BitBroker leadership team. We promise to listen, to care and to help resolve the matter in the quickest way possible and in a manner which preserves your confidentiality.

#### Consequences

Participants asked to stop any unacceptable behaviour are expected to comply immediately. If a participant continues violates this policy, the BitBroker team reserves the right to remove them from the project and rescind all the rights they have within GitHub and within all associated communication channels.

## Version and Release Methodology

This procedure applies to the following repositories:

* [bit-broker](https://github.com/bit-broker/bit-broker)
* [examples](https://github.com/bit-broker/examples)
* [charts](https://github.com/bit-broker/charts)
* [website](https://github.com/bit-broker/website)

These two _ancillary_ repositories, will follow a separate path (see below for details):

* [auth-service](https://github.com/bit-broker/auth-service)
* [rate-service](https://github.com/bit-broker/rate-service)

### General

BitBroker version and release methodology will follow the [semver](https://semver.org/) process. Here, the version number `MAJOR.MINOR.PATCH` increments as follows:

1. `MAJOR` version when you make _incompatible_ API changes,
1. `MINOR` version when you add functionality in a _backwards compatible_ manner, and
1. `PATCH` version when you make _backwards compatible_ bug fixes and improvements.

On accepting a component Pull Request which requires a version update per the criteria above, the [Core Team](#the-core-team) will decide when to create the appropriate tag. They will make a decision based upon their wide knowledge of the current state of the repository and understanding of the state of up-coming and / or pending changes.

Once tagged, this will trigger the automatic creation of component docker images, with corresponding version tags. Announcements of new tags, will be made here and on our [Twitter](https://twitter.com/broker_bit) account.

### Maintaining Previous Versions

We endeavor to keep the previous version of BitBroker operational and in good-order, wherever possible. We may, for example, create branches from previous version tags, in order to apply minor fixes or improvements. Decisions on this will be made by the [Core Team](#the-core-team) and announcements made here.

### BitBroker Core Service

As the `coordinator`, `contributor` and `consumer` services are in a common repository, they will share the same version numbers. This is true even when changes have been made that only affect one of the services.

### API versioning

Incompatible REST API changes will require a new REST API version in the API URLs. As the `coordinator`, `contributor` and `consumer` services implement the BitBroker REST API, the major version of these components to track the REST API version.

### Database

We are using flyway to handle database schema versioning and migration. We will manage schema versioning independently of component versioning. All database schema changes will require a tested database migration script.

### Ancillary Services

The [auth-service](https://github.com/bit-broker/auth-service) and [rate-service](https://github.com/bit-broker/rate-service) are ancillary services. These are used-by, but not strictly part-of BitBroker. Hence these two components will follow their own release process. However, they will still follow the same [semver](https://semver.org/) methodology outlined above. 

Changes to these services will be announced here and on our [Twitter](https://twitter.com/broker_bit) account.

### Current Release Status

#### Core Repositories

Repo | Latest Release
--- | ---
[bit-broker](https://github.com/bit-broker/bit-broker) | [v1.0.0](https://github.com/bit-broker/bit-broker/tree/v1.0.0)
[examples](https://github.com/bit-broker/examples) | [v1.0.0](https://github.com/bit-broker/examples/tree/v1.0.0)
[charts](https://github.com/bit-broker/charts) | [v1.0.0](https://github.com/bit-broker/charts/tree/v1.0.0)
[website](https://github.com/bit-broker/website) | [v1.0.0](https://github.com/bit-broker/website/tree/v1.0.0)

#### Ancillary Repositories

Repo | Latest Release
--- | ---
[auth-service](https://github.com/bit-broker/auth-service) | [v1.0.0](https://github.com/bit-broker/auth-service/tree/v1.0.0)
[rate-service](https://github.com/bit-broker/rate-service) | [v1.0.0](https://github.com/bit-broker/rate-service/tree/v1.0.0)

