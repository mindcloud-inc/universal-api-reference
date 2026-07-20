# <img src="https://images.mindcloud.co/apps/icons/unleash-icon_1776801360560.png" alt="Unleash logo" width="28" height="28"> Unleash: Universal API

Unleash is a feature management platform for managing feature flags, projects, environments, strategies, segments, API tokens, users, and operational insights through the Unleash API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/unleash/latest
- **Actions:** 376
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.getunleash.io
- **Vendor API docs:** https://docs.getunleash.io/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get projects](actions/get-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleash/latest/actions/get-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (376)

### [beta] Add Or Update Legal Value For The Context Field

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Add Or Update Legal Value For The Context Field](actions/updatecontextfieldlegalvalueforproject.md) | POST | Adds or update legal value for the context field in Unleash. |

### [beta] Call A Signal Endpoint.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Call A Signal Endpoint.](actions/callsignalendpoint.md) | POST | Calls a signal endpoint in Unleash. |

### [beta] Change A Feature Environment Safeguard

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Change A Feature Environment Safeguard](actions/changefeatureenvsafeguard.md) | PUT | Changes a feature environment safeguard in Unleash. |

### [beta] Change A Release Plan Safeguard

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Change A Release Plan Safeguard](actions/changereleaseplansafeguard.md) | PUT | Changes a release plan safeguard in Unleash. |

### [beta] Configuration For The Actions Ui.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Configuration For The Actions Ui.](actions/getactionsconfig.md) | GET | Retrieves the actions UI configuration from Unleash. |

### [beta] Connect To The Streaming Api.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Connect To The Streaming Api.](actions/connect.md) | GET | Connects to the streaming API in Unleash. |

### [beta] Create A Context Field

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Create A Context Field](actions/createcontextfieldforproject.md) | POST | Creates a context field in Unleash. |

### [beta] Create A Feature Link

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Create A Feature Link](actions/createfeaturelink.md) | POST | Creates a feature link in Unleash. |

### [beta] Create A Signal Endpoint Token For A Specific Signal Endpoint.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Create A Signal Endpoint Token For A Specific Signal Endpoint.](actions/createsignalendpointtoken.md) | POST | Creates a signal endpoint token for a specific signal endpoint in Unleash. |

### [beta] Create A Signal Endpoint.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Create A Signal Endpoint.](actions/createsignalendpoint.md) | POST | Creates a signal endpoint in Unleash. |

### [beta] Create An Action Set.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Create An Action Set.](actions/createactions.md) | POST | Creates an action set in Unleash. |

### [beta] Create Or Update A Milestone Progression

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Create Or Update A Milestone Progression](actions/changemilestoneprogression.md) | PUT | Creates new or update a milestone progression in Unleash. |

### [beta] Delete A Feature Environment Safeguard

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Delete A Feature Environment Safeguard](actions/deletefeatureenvsafeguard.md) | DELETE | Deletes a feature environment safeguard from Unleash. |

### [beta] Delete A Feature Link

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Delete A Feature Link](actions/deletefeaturelink.md) | DELETE | Deletes a feature link from Unleash. |

### [beta] Delete A Milestone Progression

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Delete A Milestone Progression](actions/deletemilestoneprogression.md) | DELETE | Deletes a milestone progression from Unleash. |

### [beta] Delete A Release Plan Safeguard

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Delete A Release Plan Safeguard](actions/deletereleaseplansafeguard.md) | DELETE | Deletes a release plan safeguard from Unleash. |

### [beta] Delete A Signal Endpoint Token.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Delete A Signal Endpoint Token.](actions/deletesignalendpointtoken.md) | DELETE | Deletes a signal endpoint token from Unleash. |

### [beta] Delete A Signal Endpoint.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Delete A Signal Endpoint.](actions/deletesignalendpoint.md) | DELETE | Deletes a signal endpoint from Unleash. |

### [beta] Delete An Action Set.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Delete An Action Set.](actions/deleteactions.md) | DELETE | Deletes an action set from Unleash. |

### [beta] Delete An Existing Context Field

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Delete An Existing Context Field](actions/deletecontextfieldforproject.md) | DELETE | Deletes an existing context field from Unleash. |

### [beta] Delete Flag Level Impact Metric Configuration

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Delete Flag Level Impact Metric Configuration](actions/deleteflagimpactmetricconfig.md) | DELETE | Deletes flag level impact metric configuration from Unleash. |

### [beta] Delete Instance Level Impact Metric Configuration

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Delete Instance Level Impact Metric Configuration](actions/deleteinstanceimpactmetricconfig.md) | DELETE | Deletes instance level impact metric configuration from Unleash. |

### [beta] Delete Legal Value For The Context Field

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Delete Legal Value For The Context Field](actions/deletecontextfieldlegalvalueforproject.md) | DELETE | Deletes legal value for the context field from Unleash. |

### [beta] Disables A Signal Endpoint.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Disables A Signal Endpoint.](actions/disablesignalendpoint.md) | POST | Disables a signal endpoint in Unleash. |

### [beta] Disables An Action Set.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Disables An Action Set.](actions/disableactions.md) | POST | Disables an action set in Unleash. |

### [beta] Disconnect All Clients.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Disconnect All Clients.](actions/disconnectall.md) | POST | Disconnects all clients in Unleash. |

### [beta] Enables A Signal Endpoint.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Enables A Signal Endpoint.](actions/enablesignalendpoint.md) | POST | Enables a signal endpoint in Unleash. |

### [beta] Enables An Action Set.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Enables An Action Set.](actions/enableactions.md) | POST | Enables an action set in Unleash. |

### [beta] Get Action Events For A Specific Action Set.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Action Events For A Specific Action Set.](actions/getactionsevents.md) | GET | Retrieves action events for a specific action set from Unleash. |

### [beta] Get Aggregated Metered Connections For A Given Time Period.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Aggregated Metered Connections For A Given Time Period.](actions/getconnectionsforperiod.md) | GET | Retrieves aggregated metered connections for a given time period from Unleash. |

### [beta] Get Aggregated Metered Requests For A Given Time Period.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Aggregated Metered Requests For A Given Time Period.](actions/getrequestsforperiod.md) | GET | Retrieves aggregated metered requests for a given time period from Unleash. |

### [beta] Get All Features Lifecycle Stage Count

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get All Features Lifecycle Stage Count](actions/getfeaturelifecyclestagecount.md) | GET | Retrieves features lifecycle stage count from Unleash. |

### [beta] Get All Signal Endpoint Tokens For A Specific Signal Endpoint.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get All Signal Endpoint Tokens For A Specific Signal Endpoint.](actions/getsignalendpointtokens.md) | GET | Retrieves signal endpoint tokens for a specific signal endpoint from Unleash. |

### [beta] Get All Signal Endpoints.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get All Signal Endpoints.](actions/getsignalendpoints.md) | GET | Retrieves signal endpoints from Unleash. |

### [beta] Get All Signals That Match The Query Parameter Criteria.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get All Signals That Match The Query Parameter Criteria.](actions/getsignals.md) | GET | Retrieves signals that match the query parameter criteria from Unleash. |

### [beta] Get Feature Lifecycle

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Feature Lifecycle](actions/getfeaturelifecycle.md) | GET | Retrieves feature lifecycle from Unleash. |

### [beta] Get Impact Metrics Configuration For The Instance

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Impact Metrics Configuration For The Instance](actions/getinstanceimpactmetricsconfigs.md) | GET | Retrieves impact metrics configuration for the instance from Unleash. |

### [beta] Get Impact Metrics Configurations For A Single Feature

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Impact Metrics Configurations For A Single Feature](actions/getflagimpactmetricsconfigsbyfeature.md) | GET | Retrieves impact metrics configurations for a single feature from Unleash. |

### [beta] Get Partial Updates (sdk)

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Partial Updates (Sdk)](actions/get-api-client-delta.md) | GET | Retrieves partial updates SDK from Unleash. |

### [beta] Get Personal Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Personal Dashboard](actions/getpersonaldashboard.md) | GET | Retrieves personal dashboard from Unleash. |

### [beta] Get Personal Project Details

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Personal Project Details](actions/getpersonaldashboardprojectdetails.md) | GET | Retrieves personal project details from Unleash. |

### [beta] Get Project Status

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Project Status](actions/getprojectstatus.md) | GET | Retrieves project status from Unleash. |

### [beta] Get Signals Originated From A Specific Signal Endpoint.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Signals Originated From A Specific Signal Endpoint.](actions/getsignalendpointsignals.md) | GET | Retrieves signals originated from a specific signal endpoint from Unleash. |

### [beta] Get Strategies That Use A Context Field

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Get Strategies That Use A Context Field](actions/getstrategiesbycontextfieldforproject.md) | GET | Retrieves strategies that use a context field from Unleash. |

### [beta] Gets Configured Context Fields

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Gets Configured Context Fields](actions/getcontextfieldsforproject.md) | GET | Retrieves configured context fields from Unleash. |

### [beta] Gets Context Field

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Gets Context Field](actions/getcontextfieldforproject.md) | GET | Retrieves context field from Unleash. |

### [beta] List Action Sets.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] List Action Sets.](actions/getactions.md) | GET | Retrieves action sets from Unleash. |

### [beta] Resume Paused Milestone Progressions

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Resume Paused Milestone Progressions](actions/resumemilestoneprogressions.md) | POST | Resumes paused milestone progressions in Unleash. |

### [beta] Save Flag Level Impact Metrics Configuration

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Save Flag Level Impact Metrics Configuration](actions/savefeatureimpactmetricsconfig.md) | POST | Saves flag-level impact metrics configuration in Unleash. |

### [beta] Save Instance Level Impact Metrics Configuration

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Save Instance Level Impact Metrics Configuration](actions/saveinstanceimpactmetricsconfig.md) | POST | Saves instance-level impact metrics configuration in Unleash. |

### [beta] Set Feature Completed

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Set Feature Completed](actions/complete.md) | POST | Sets feature completed in Unleash. |

### [beta] Set Feature Uncompleted

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Set Feature Uncompleted](actions/uncomplete.md) | POST | Sets feature uncompleted in Unleash. |

### [beta] Subscribe To Email Subscription

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Subscribe To Email Subscription](actions/subscribeemailsubscription.md) | PUT | Subscribes to an email subscription in Unleash. |

### [beta] Unsubscribe From Email Subscription

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Unsubscribe From Email Subscription](actions/unsubscribeemailsubscription.md) | DELETE | Unsubscribes from an email subscription in Unleash. |

### [beta] Update A Feature Link

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Update A Feature Link](actions/updatefeaturelink.md) | PUT | Updates a feature link in Unleash. |

### [beta] Update A Milestone Strategy

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Update A Milestone Strategy](actions/updateprojectmilestonestrategy.md) | PUT | Updates a milestone strategy in Unleash. |

### [beta] Update A Signal Endpoint Token.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Update A Signal Endpoint Token.](actions/updatesignalendpointtoken.md) | PUT | Updates a signal endpoint token in Unleash. |

### [beta] Update A Signal Endpoint.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Update A Signal Endpoint.](actions/updatesignalendpoint.md) | PUT | Updates a signal endpoint in Unleash. |

### [beta] Update An Action Set.

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Update An Action Set.](actions/updateactions.md) | PUT | Updates an action set in Unleash. |

### [beta] Update An Existing Context Field

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Update An Existing Context Field](actions/updatecontextfieldforproject.md) | PUT | Updates an existing context field in Unleash. |

### [beta] Validate A Context Field

| Action | Method | Description |
| --- | --- | --- |
| [[Beta] Validate A Context Field](actions/validatecontextfieldnameforproject.md) | POST | Validates a context field in Unleash. |

### Accepts Errors From The Ui Client

| Action | Method | Description |
| --- | --- | --- |
| [Accepts Errors From The Ui Client](actions/uiobservability.md) | POST | Accepts errors from the UI client in Unleash. |

### Add A Feature Dependency.

| Action | Method | Description |
| --- | --- | --- |
| [Add A Feature Dependency.](actions/addfeaturedependency.md) | POST | Adds a feature dependency in Unleash. |

### Add A New Feature Flag

| Action | Method | Description |
| --- | --- | --- |
| [Add A New Feature Flag](actions/createfeature.md) | POST | Adds a new feature flag in Unleash. |

### Add A Release Plan.

| Action | Method | Description |
| --- | --- | --- |
| [Add A Release Plan.](actions/addreleaseplan.md) | POST | Adds a release plan in Unleash. |
| [Add A Release Plan.](actions/oldaddreleaseplan.md) | POST |  |

### Add A Strategy To A Feature Flag

| Action | Method | Description |
| --- | --- | --- |
| [Add A Strategy To A Feature Flag](actions/addfeaturestrategy.md) | POST | Adds a strategy to a feature flag in Unleash. |

### Add A User Via A Signup Token

| Action | Method | Description |
| --- | --- | --- |
| [Add A User Via A Signup Token](actions/addpublicsignuptokenuser.md) | POST | Adds a user via a signup token in Unleash. |

### Add An Environment To A Project.

| Action | Method | Description |
| --- | --- | --- |
| [Add An Environment To A Project.](actions/addenvironmenttoproject.md) | POST | Adds an environment to a project in Unleash. |

### Add Feature To Favorites

| Action | Method | Description |
| --- | --- | --- |
| [Add Feature To Favorites](actions/addfavoritefeature.md) | POST | Adds a feature to favorites in Unleash. |

### Add Or Update Legal Value For The Context Field

| Action | Method | Description |
| --- | --- | --- |
| [Add Or Update Legal Value For The Context Field](actions/updatecontextfieldlegalvalue.md) | POST | Adds or update legal value for the context field in Unleash. |

### Add Project To Favorites

| Action | Method | Description |
| --- | --- | --- |
| [Add Project To Favorites](actions/addfavoriteproject.md) | POST | Adds a project to favorites in Unleash. |

### Adds A Milestone To A Release Template.

| Action | Method | Description |
| --- | --- | --- |
| [Adds A Milestone To A Release Template.](actions/addmilestonetoreleasetemplate.md) | POST | Adds a milestone to a release template in Unleash. |

### Adds A Strategy To A Milestone.

| Action | Method | Description |
| --- | --- | --- |
| [Adds A Strategy To A Milestone.](actions/post-api-admin-release-plan-templates-templateid-milestones-milestoneid-strategies.md) | POST | Adds a strategy to a milestone in Unleash. |

### Adds A Tag To A Feature.

| Action | Method | Description |
| --- | --- | --- |
| [Adds A Tag To A Feature.](actions/post-api-admin-features-featurename-tags.md) | POST | Adds a tag to a feature in Unleash. |

### Adds A Tag To The Specified Features

| Action | Method | Description |
| --- | --- | --- |
| [Adds A Tag To The Specified Features](actions/addtagtofeatures.md) | PUT | Adds a tag to the specified features in Unleash. |

### Approve A User Access Request.

| Action | Method | Description |
| --- | --- | --- |
| [Approve A User Access Request.](actions/approveuseraccessrequest.md) | POST | Approves a user access request in Unleash. |

### Archive A Feature Flag

| Action | Method | Description |
| --- | --- | --- |
| [Archive A Feature Flag](actions/archivefeature.md) | DELETE | Archives a feature flag in Unleash. |

### Archive Project

| Action | Method | Description |
| --- | --- | --- |
| [Archive Project](actions/archiveproject.md) | POST | Archives a project in Unleash. |

### Archives A Feature

| Action | Method | Description |
| --- | --- | --- |
| [Archives A Feature](actions/deletefeature.md) | DELETE | Archives a feature in Unleash. |

### Archives A List Of Features

| Action | Method | Description |
| --- | --- | --- |
| [Archives A List Of Features](actions/archivefeatures.md) | POST | Archives a list of features in Unleash. |

### Archives A Release Template By Its Id.

| Action | Method | Description |
| --- | --- | --- |
| [Archives A Release Template By Its Id.](actions/archivereleasetemplate.md) | POST | Archives a release template by its id in Unleash. |

### Batch Evaluate An Unleash Context Against A Set Of Environments And Projects.

| Action | Method | Description |
| --- | --- | --- |
| [Batch Evaluate An Unleash Context Against A Set Of Environments And Projects.](actions/getadvancedplayground.md) | POST | Evaluates an Unleash context across environments and projects. |

### Bulk Disable A List Of Features

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Disable A List Of Features](actions/bulktogglefeaturesenvironmentoff.md) | POST | Disables a list of features in Unleash. |

### Bulk Enable A List Of Features

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Enable A List Of Features](actions/bulktogglefeaturesenvironmenton.md) | POST | Enables a list of features in Unleash. |

### Change Password For A User

| Action | Method | Description |
| --- | --- | --- |
| [Change Password For A User](actions/changeuserpassword.md) | POST | Changes a user's password in Unleash. |

### Change Request Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search change requests](actions/search-change-requests.md) | GET | Searches change requests in Unleash. |

### Change Specific Properties Of A Strategy

| Action | Method | Description |
| --- | --- | --- |
| [Change Specific Properties Of A Strategy](actions/patchfeaturestrategy.md) | PUT | Changes specific strategy properties in Unleash. |

### Change Your Own Password

| Action | Method | Description |
| --- | --- | --- |
| [Change Your Own Password](actions/changemypassword.md) | POST | Changes your password in Unleash. |

### Changes A User Password

| Action | Method | Description |
| --- | --- | --- |
| [Changes A User Password](actions/changepassword.md) | POST | Changes a user password in Unleash. |

### Check Dependencies Exist.

| Action | Method | Description |
| --- | --- | --- |
| [Check Dependencies Exist.](actions/checkdependenciesexist.md) | GET | Checks dependencies exist in Unleash. |

### Check Which Tokens Are Valid

| Action | Method | Description |
| --- | --- | --- |
| [Check Which Tokens Are Valid](actions/getvalidtokens.md) | POST | Checks which tokens are valid in Unleash. |

### Clone A Feature Flag

| Action | Method | Description |
| --- | --- | --- |
| [Clone A Feature Flag](actions/clonefeature.md) | POST | Clones a feature flag in Unleash. |

### Clones An Environment

| Action | Method | Description |
| --- | --- | --- |
| [Clones An Environment](actions/cloneenvironment.md) | POST | Clones an environment in Unleash. |

### Configure Project Access

| Action | Method | Description |
| --- | --- | --- |
| [Configure Project Access](actions/addaccesstoproject.md) | POST | Configures project access in Unleash. |

### Create (overwrite) Variants For A Feature Flag In Multiple Environments

| Action | Method | Description |
| --- | --- | --- |
| [Create (Overwrite) Variants For A Feature Flag In Multiple Environments](actions/overwritefeaturevariantsonenvironments.md) | PUT | Creates or overwrites feature variants across environments in Unleash. |

### Create (overwrite) Variants For A Feature In An Environment

| Action | Method | Description |
| --- | --- | --- |
| [Create (Overwrite) Variants For A Feature In An Environment](actions/overwriteenvironmentfeaturevariants.md) | PUT | Creates or overwrites feature variants in an environment in Unleash. |

### Create A Banner.

| Action | Method | Description |
| --- | --- | --- |
| [Create A Banner.](actions/createbanner.md) | POST | Creates a banner in Unleash. |

### Create A Context Field

| Action | Method | Description |
| --- | --- | --- |
| [Create A Context Field](actions/createcontextfield.md) | POST | Creates a context field in Unleash. |

### Create A New Addon

| Action | Method | Description |
| --- | --- | --- |
| [Create A New Addon](actions/createaddon.md) | POST | Creates a new addon in Unleash. |

### Create A New Group

| Action | Method | Description |
| --- | --- | --- |
| [Create A New Group](actions/creategroup.md) | POST | Creates a new group in Unleash. |

### Create A New Personal Access Token (pat) For The Current User.

| Action | Method | Description |
| --- | --- | --- |
| [Create A New Personal Access Token (Pat) For The Current User.](actions/createpat.md) | POST | Creates a new personal access token (PAT) for the current user in Unleash. |

### Create A New Role

| Action | Method | Description |
| --- | --- | --- |
| [Create A New Role](actions/createrole.md) | POST | Creates a new role in Unleash. |

### Create A New Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create A New Segment](actions/createsegment.md) | POST | Creates a new segment in Unleash. |

### Create A New Tag.

| Action | Method | Description |
| --- | --- | --- |
| [Create A New Tag.](actions/createtag.md) | POST | Creates a new tag in Unleash. |

### Create A New User

| Action | Method | Description |
| --- | --- | --- |
| [Create A New User](actions/createuser.md) | POST | Creates a new user in Unleash. |

### Create A Project Api Token.

| Action | Method | Description |
| --- | --- | --- |
| [Create A Project Api Token.](actions/createprojectapitoken.md) | POST | Creates a project API token in Unleash. |

### Create A Public Signup Token

| Action | Method | Description |
| --- | --- | --- |
| [Create A Public Signup Token](actions/createpublicsignuptoken.md) | POST | Creates a public signup token in Unleash. |

### Create A Release Template.

| Action | Method | Description |
| --- | --- | --- |
| [Create A Release Template.](actions/createreleasetemplate.md) | POST | Creates a release template in Unleash. |

### Create A Service Account.

| Action | Method | Description |
| --- | --- | --- |
| [Create A Service Account.](actions/createserviceaccount.md) | POST | Creates a service account in Unleash. |

### Create A Strategy

| Action | Method | Description |
| --- | --- | --- |
| [Create A Strategy](actions/post-api-admin-strategies.md) | POST | Creates a strategy in Unleash. |

### Create A Tag Type

| Action | Method | Description |
| --- | --- | --- |
| [Create A Tag Type](actions/createtagtype.md) | POST | Creates a tag type in Unleash. |

### Create A Token For A Service Account.

| Action | Method | Description |
| --- | --- | --- |
| [Create A Token For A Service Account.](actions/createserviceaccounttoken.md) | POST | Creates a token for a service account in Unleash. |

### Create An Application To Connect Reported Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Create An Application To Connect Reported Metrics](actions/createapplication.md) | POST | Creates an application to connect reported metrics in Unleash. |

### Create Api Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Api Token](actions/createapitoken.md) | POST | Creates a new API token in Unleash. |

### Create Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/createproject.md) | POST | Creates a new project in Unleash. |

### Create/add Change To A Change Request

| Action | Method | Description |
| --- | --- | --- |
| [Create/Add Change To A Change Request](actions/changerequest.md) | POST | Creates or adds a change to a request in Unleash. |

### Creates A New Environment

| Action | Method | Description |
| --- | --- | --- |
| [Creates A New Environment](actions/createenvironment.md) | POST | Creates a new environment in Unleash. |

### Delete A Banner.

| Action | Method | Description |
| --- | --- | --- |
| [Delete A Banner.](actions/deletebanner.md) | DELETE | Deletes a banner from Unleash. |

### Delete A Custom Role

| Action | Method | Description |
| --- | --- | --- |
| [Delete A Custom Role](actions/deleterole.md) | DELETE | Deletes a custom role from Unleash. |

### Delete A Personal Access Token (pat) For The Current User.

| Action | Method | Description |
| --- | --- | --- |
| [Delete A Personal Access Token (Pat) For The Current User.](actions/deletepat.md) | DELETE | Deletes a personal access token (PAT) for the current user from Unleash. |

### Delete A Project Api Token.

| Action | Method | Description |
| --- | --- | --- |
| [Delete A Project Api Token.](actions/deleteprojectapitoken.md) | DELETE | Deletes a project API token from Unleash. |

### Delete A Service Account.

| Action | Method | Description |
| --- | --- | --- |
| [Delete A Service Account.](actions/deleteserviceaccount.md) | DELETE | Deletes a service account from Unleash. |

### Delete A Single Group

| Action | Method | Description |
| --- | --- | --- |
| [Delete A Single Group](actions/deletegroup.md) | DELETE | Deletes a single group from Unleash. |

### Delete A Strategy

| Action | Method | Description |
| --- | --- | --- |
| [Delete A Strategy](actions/delete-api-admin-strategies-name.md) | DELETE | Deletes a strategy from Unleash. |

### Delete A Strategy From A Feature Flag

| Action | Method | Description |
| --- | --- | --- |
| [Delete A Strategy From A Feature Flag](actions/deletefeaturestrategy.md) | DELETE | Deletes a strategy from a feature flag from Unleash. |

### Delete A Tag Type

| Action | Method | Description |
| --- | --- | --- |
| [Delete A Tag Type](actions/deletetagtype.md) | DELETE | Deletes a tag type from Unleash. |

### Delete A Tag.

| Action | Method | Description |
| --- | --- | --- |
| [Delete A Tag.](actions/deletetag.md) | DELETE | Deletes a tag from Unleash. |

### Delete A Token For A Service Account.

| Action | Method | Description |
| --- | --- | --- |
| [Delete A Token For A Service Account.](actions/deleteserviceaccounttoken.md) | DELETE | Deletes a token for a service account from Unleash. |

### Delete A User

| Action | Method | Description |
| --- | --- | --- |
| [Delete A User](actions/deleteuser.md) | DELETE | Deletes a user from Unleash. |

### Delete All Scim Groups

| Action | Method | Description |
| --- | --- | --- |
| [Delete All Scim Groups](actions/deletescimgroups.md) | DELETE | Deletes all SCIM groups from Unleash. |

### Delete All Scim Users

| Action | Method | Description |
| --- | --- | --- |
| [Delete All Scim Users](actions/deletescimusers.md) | DELETE | Deletes all SCIM users from Unleash. |

### Delete An Addon

| Action | Method | Description |
| --- | --- | --- |
| [Delete An Addon](actions/deleteaddon.md) | DELETE | Deletes an addon from Unleash. |

### Delete An Application

| Action | Method | Description |
| --- | --- | --- |
| [Delete An Application](actions/deleteapplication.md) | DELETE | Deletes an application from Unleash. |

### Delete An Existing Context Field

| Action | Method | Description |
| --- | --- | --- |
| [Delete An Existing Context Field](actions/deletecontextfield.md) | DELETE | Deletes an existing context field from Unleash. |

### Delete Api Token

| Action | Method | Description |
| --- | --- | --- |
| [Delete Api Token](actions/deleteapitoken.md) | DELETE | Deletes an API token from Unleash. |

### Delete Legal Value For The Context Field

| Action | Method | Description |
| --- | --- | --- |
| [Delete Legal Value For The Context Field](actions/deletecontextfieldlegalvalue.md) | DELETE | Deletes legal value for the context field from Unleash. |

### Delete Project

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project](actions/deleteproject.md) | DELETE | Deletes a project from Unleash. |

### Deletes A Change Request By Id

| Action | Method | Description |
| --- | --- | --- |
| [Deletes A Change Request By Id](actions/deletechangerequest.md) | DELETE | Deletes a change request by id from Unleash. |

### Deletes A Feature Dependency.

| Action | Method | Description |
| --- | --- | --- |
| [Deletes A Feature Dependency.](actions/deletefeaturedependency.md) | DELETE | Deletes a feature dependency from Unleash. |

### Deletes A List Of Features

| Action | Method | Description |
| --- | --- | --- |
| [Deletes A List Of Features](actions/deletefeatures.md) | POST | Deletes a list of features from Unleash. |

### Deletes A Release Template By Its Id.

| Action | Method | Description |
| --- | --- | --- |
| [Deletes A Release Template By Its Id.](actions/deletereleasetemplate.md) | DELETE | Deletes a release template by its id from Unleash. |

### Deletes A Segment By Id

| Action | Method | Description |
| --- | --- | --- |
| [Deletes A Segment By Id](actions/removesegment.md) | DELETE | Deletes a segment by id from Unleash. |

### Deletes An Environment By Name

| Action | Method | Description |
| --- | --- | --- |
| [Deletes An Environment By Name](actions/removeenvironment.md) | DELETE | Deletes an environment by name from Unleash. |

### Deletes Feature Dependencies.

| Action | Method | Description |
| --- | --- | --- |
| [Deletes Feature Dependencies.](actions/deletefeaturedependencies.md) | DELETE | Deletes a feature dependencies from Unleash. |

### Deletes Inactive Users

| Action | Method | Description |
| --- | --- | --- |
| [Deletes Inactive Users](actions/deleteinactiveusers.md) | POST | Deletes an inactive users from Unleash. |

### Deprecate A Strategy

| Action | Method | Description |
| --- | --- | --- |
| [Deprecate A Strategy](actions/post-api-admin-strategies-strategyname-deprecate.md) | POST | Deprecates a strategy in Unleash. |

### Disable A Feature Flag

| Action | Method | Description |
| --- | --- | --- |
| [Disable A Feature Flag](actions/togglefeatureenvironmentoff.md) | POST | Disables a feature flag in Unleash. |

### Disables A Banner.

| Action | Method | Description |
| --- | --- | --- |
| [Disables A Banner.](actions/disablebanner.md) | POST | Disables a banner in Unleash. |

### Discards A Change From A Change Request By Change Id

| Action | Method | Description |
| --- | --- | --- |
| [Discards A Change From A Change Request By Change Id](actions/deletechange.md) | DELETE | Discards a change from a change request by change id in Unleash. |

### Edits A Single Change In A Change Request

| Action | Method | Description |
| --- | --- | --- |
| [Edits A Single Change In A Change Request](actions/editchange.md) | PUT | Edits a single change in a change request in Unleash. |

### Enable A Feature Flag

| Action | Method | Description |
| --- | --- | --- |
| [Enable A Feature Flag](actions/togglefeatureenvironmenton.md) | POST | Enables a feature flag in Unleash. |

### Enabled/disabled Maintenance Mode

| Action | Method | Description |
| --- | --- | --- |
| [Enabled/Disabled Maintenance Mode](actions/togglemaintenance.md) | POST | Toggles maintenance mode in Unleash. |

### Enables A Banner.

| Action | Method | Description |
| --- | --- | --- |
| [Enables A Banner.](actions/enablebanner.md) | POST | Enables a banner in Unleash. |

### Evaluate An Unleash Context Against A Change Request Preview.

| Action | Method | Description |
| --- | --- | --- |
| [Evaluate An Unleash Context Against A Change Request Preview.](actions/getchangerequestplayground.md) | POST | Evaluates a change request preview against an Unleash context. |

### Evaluate An Unleash Context Against A Set Of Environments And Projects.

| Action | Method | Description |
| --- | --- | --- |
| [Evaluate An Unleash Context Against A Set Of Environments And Projects.](actions/getplayground.md) | POST | Evaluates an Unleash context across environments and projects. |

### Export Feature Flags From An Environment

| Action | Method | Description |
| --- | --- | --- |
| [Export Feature Flags From An Environment](actions/post-api-admin-features-batch-export.md) | POST | Exports feature flags from an environment in Unleash. |

### Generates A New Scim Api Token.

| Action | Method | Description |
| --- | --- | --- |
| [Generates A New Scim Api Token.](actions/generatenewtoken.md) | POST | Generates a new SCIM API token in Unleash. |

### Get A Feature

| Action | Method | Description |
| --- | --- | --- |
| [Get A Feature](actions/getfeature.md) | GET | Retrieves a feature from Unleash. |

### Get A Feature Environment

| Action | Method | Description |
| --- | --- | --- |
| [Get A Feature Environment](actions/getfeatureenvironment.md) | GET | Retrieves a feature environment from Unleash. |

### Get A Health Report For A Project.

| Action | Method | Description |
| --- | --- | --- |
| [Get A Health Report For A Project.](actions/getprojecthealthreport.md) | GET | Retrieves a health report for a project from Unleash. |

### Get A List Of All Applications For A Project.

| Action | Method | Description |
| --- | --- | --- |
| [Get A List Of All Applications For A Project.](actions/getprojectapplications.md) | GET | Retrieves applications for a project from Unleash. |

### Get A List Of All Flag Creators For A Project.

| Action | Method | Description |
| --- | --- | --- |
| [Get A List Of All Flag Creators For A Project.](actions/getprojectflagcreators.md) | GET | Retrieves flag creators for a project from Unleash. |

### Get A List Of All Users That Have Created Events

| Action | Method | Description |
| --- | --- | --- |
| [Get A List Of All Users That Have Created Events](actions/geteventcreators.md) | GET | Retrieves users that have created events from Unleash. |

### Get A List Of Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get A List Of Groups](actions/getgroups.md) | GET | Retrieves groups from Unleash. |

### Get A List Of Roles

| Action | Method | Description |
| --- | --- | --- |
| [Get A List Of Roles](actions/getroles.md) | GET | Retrieves roles from Unleash. |

### Get A Release Template By Its Id.

| Action | Method | Description |
| --- | --- | --- |
| [Get A Release Template By Its Id.](actions/getreleasetemplate.md) | GET | Retrieves a release template by its id from Unleash. |

### Get A Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get A Segment](actions/getsegment.md) | GET | Retrieves a segment from Unleash. |

### Get A Single Feature Flag

| Action | Method | Description |
| --- | --- | --- |
| [Get A Single Feature Flag](actions/get-api-client-features-featurename.md) | GET | Retrieves a feature flag from Unleash. |

### Get A Single Group

| Action | Method | Description |
| --- | --- | --- |
| [Get A Single Group](actions/getgroup.md) | GET | Retrieves a group from Unleash. |

### Get A Single Role

| Action | Method | Description |
| --- | --- | --- |
| [Get A Single Role](actions/getrolebyid.md) | GET | Retrieves a role from Unleash. |

### Get A Specific Addon

| Action | Method | Description |
| --- | --- | --- |
| [Get A Specific Addon](actions/getaddon.md) | GET | Retrieves a specific addon from Unleash. |

### Get A Strategy Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get A Strategy Configuration](actions/getfeaturestrategy.md) | GET | Retrieves a strategy configuration from Unleash. |

### Get A Strategy Definition

| Action | Method | Description |
| --- | --- | --- |
| [Get A Strategy Definition](actions/get-api-admin-strategies-name.md) | GET | Retrieves a strategy definition from Unleash. |

### Get A Tag By Type And Value.

| Action | Method | Description |
| --- | --- | --- |
| [Get A Tag By Type And Value.](actions/gettag.md) | GET | Retrieves a tag by type and value from Unleash. |

### Get A Tag Type

| Action | Method | Description |
| --- | --- | --- |
| [Get A Tag Type](actions/gettagtype.md) | GET | Retrieves a tag type from Unleash. |

### Get Aggregated Traffic Data For A Given Time Period.

| Action | Method | Description |
| --- | --- | --- |
| [Get Aggregated Traffic Data For A Given Time Period.](actions/gettrafficdatausageforperiod.md) | GET | Retrieves aggregated traffic data for a given time period from Unleash. |

### Get All Addons And Providers

| Action | Method | Description |
| --- | --- | --- |
| [Get All Addons And Providers](actions/getaddons.md) | GET | Retrieves addons and providers from Unleash. |

### Get All Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get All Applications](actions/getapplications.md) | GET | Retrieves applications from Unleash. |

### Get All Banners.

| Action | Method | Description |
| --- | --- | --- |
| [Get All Banners.](actions/getbanners.md) | GET | Retrieves banners from Unleash. |

### Get All Environments

| Action | Method | Description |
| --- | --- | --- |
| [Get All Environments](actions/getallenvironments.md) | GET | Retrieves environments from Unleash. |

### Get All Events Related To A Specific Feature Flag.

| Action | Method | Description |
| --- | --- | --- |
| [Get All Events Related To A Specific Feature Flag.](actions/geteventsfortoggle.md) | GET | Retrieves events related to a specific feature flag from Unleash. |

### Get All Feature Types

| Action | Method | Description |
| --- | --- | --- |
| [Get All Feature Types](actions/get-api-admin-feature-types.md) | GET | Retrieves feature types from Unleash. |

### Get All Features In A Project

| Action | Method | Description |
| --- | --- | --- |
| [Get All Features In A Project](actions/getfeatures.md) | GET | Retrieves features in a project from Unleash. |

### Get All Flags (sdk)

| Action | Method | Description |
| --- | --- | --- |
| [Get All Flags (Sdk)](actions/get-api-client-features.md) | GET | Retrieves all feature flags for SDKs from Unleash. |

### Get All Login Events.

| Action | Method | Description |
| --- | --- | --- |
| [Get All Login Events.](actions/getloginhistory.md) | GET | Retrieves login events from Unleash. |

### Get All Pending User Access Requests.

| Action | Method | Description |
| --- | --- | --- |
| [Get All Pending User Access Requests.](actions/getuseraccessrequests.md) | GET | Retrieves pending user access requests from Unleash. |

### Get All Personal Access Tokens (pats) For The Current User.

| Action | Method | Description |
| --- | --- | --- |
| [Get All Personal Access Tokens (Pats) For The Current User.](actions/getpats.md) | GET | Retrieves personal access tokens (PATs) for the current user from Unleash. |

### Get All Release Templates.

| Action | Method | Description |
| --- | --- | --- |
| [Get All Release Templates.](actions/getreleasetemplates.md) | GET | Retrieves release templates from Unleash. |

### Get All Segments

| Action | Method | Description |
| --- | --- | --- |
| [Get All Segments](actions/getsegments.md) | GET | Retrieves segments from Unleash. |

### Get All Strategies

| Action | Method | Description |
| --- | --- | --- |
| [Get All Strategies](actions/get-api-admin-strategies.md) | GET | Retrieves strategies from Unleash. |

### Get All Tag Types

| Action | Method | Description |
| --- | --- | --- |
| [Get All Tag Types](actions/gettagtypes.md) | GET | Retrieves tag types from Unleash. |

### Get All Tags For A Feature.

| Action | Method | Description |
| --- | --- | --- |
| [Get All Tags For A Feature.](actions/get-api-admin-features-featurename-tags.md) | GET | Retrieves tags for a feature from Unleash. |

### Get All Users And [root Roles](https://docs.getunleash.io/concepts/rbac#predefin

| Action | Method | Description |
| --- | --- | --- |
| [Get All Users And [Root Roles](Https://Docs.Getunleash.Io/Concepts/Rbac#Predefin](actions/getusers.md) | GET | Retrieves users and [root roles](https://docs.getunleash.io/concepts/rbac#predefined-roles) from Unleash. |

### Get An Overview Of A Project Insights.

| Action | Method | Description |
| --- | --- | --- |
| [Get An Overview Of A Project Insights.](actions/getprojectinsights.md) | GET | Retrieves an overview of a project insights from Unleash. |

### Get An Overview Of A Project.

| Action | Method | Description |
| --- | --- | --- |
| [Get An Overview Of A Project.](actions/getprojectoverview.md) | GET | Retrieves an overview of a project from Unleash. |

### Get An Overview Project Dora Metrics.

| Action | Method | Description |
| --- | --- | --- |
| [Get An Overview Project Dora Metrics.](actions/getprojectdora.md) | GET | Retrieves an overview project dora metrics from Unleash. |

### Get Api Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Api Tokens](actions/getallapitokens.md) | GET | Retrieves API tokens from Unleash. |

### Get Api Tokens By Name

| Action | Method | Description |
| --- | --- | --- |
| [Get Api Tokens By Name](actions/getapitokensbyname.md) | GET | Retrieves API tokens by name from Unleash. |

### Get Api Tokens For Project.

| Action | Method | Description |
| --- | --- | --- |
| [Get Api Tokens For Project.](actions/getprojectapitokens.md) | GET | Retrieves api tokens for project from Unleash. |

### Get Application Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Data](actions/getapplication.md) | GET | Retrieves application data from Unleash. |

### Get Application Environment Instances (last 24h)

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Environment Instances (Last 24H)](actions/getapplicationenvironmentinstances.md) | GET | Retrieves application environment instances (Last 24h) from Unleash. |

### Get Application Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Overview](actions/getapplicationoverview.md) | GET | Retrieves application overview from Unleash. |

### Get Basic User And Group Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Basic User And Group Information](actions/getbaseusersandgroups.md) | GET | Retrieves basic user and group information from Unleash. |

### Get Detailed Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Detailed Invoices](actions/getdetailedinvoices.md) | GET | Retrieves Detailed Invoices from Unleash. |

### Get Feature Flag Strategies

| Action | Method | Description |
| --- | --- | --- |
| [Get Feature Flag Strategies](actions/getfeaturestrategies.md) | GET | Retrieves feature flag strategies from Unleash. |

### Get Feature Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Feature Metrics](actions/getrawfeaturemetrics.md) | GET | Retrieves feature metrics from Unleash. |

### Get Instance Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Instance Information](actions/getinstanceinsights.md) | GET | Retrieves instance information from Unleash. |

### Get Instance Operational Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Instance Operational Status](actions/gethealth.md) | GET | Retrieves instance operational status from Unleash. |

### Get Instance Readiness Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Instance Readiness Status](actions/getready.md) | GET | Retrieves instance readiness status from Unleash. |

### Get Integration Events For A Specific Integration Configuration.

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration Events For A Specific Integration Configuration.](actions/getintegrationevents.md) | GET | Retrieves integration events for a specific integration configuration from Unleash. |

### Get Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoices](actions/getinvoices.md) | GET | Retrieves Invoices from Unleash. |

### Get Lifecycle Trends

| Action | Method | Description |
| --- | --- | --- |
| [Get Lifecycle Trends](actions/getlifecycletrends.md) | GET | Retrieves lifecycle trends from Unleash. |

### Get Maintenance Mode Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Maintenance Mode Status](actions/getmaintenance.md) | GET | Retrieves maintenance mode status from Unleash. |

### Get Metrics In Prometheus Format

| Action | Method | Description |
| --- | --- | --- |
| [Get Metrics In Prometheus Format](actions/getprometheusmetrics.md) | GET | Retrieves metrics in Prometheus format from Unleash. |

### Get Oidc Auth Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Oidc Auth Settings](actions/getoidcsettings.md) | GET | Retrieves OIDC auth settings from Unleash. |

### Get Or Create Valid Tokens For The Requested Environment

| Action | Method | Description |
| --- | --- | --- |
| [Get Or Create Valid Tokens For The Requested Environment](actions/edgecreateorreturntokens.md) | POST | Retrieves or creates valid tokens for an environment in Unleash. |

### Get Outdated Project Sdks

| Action | Method | Description |
| --- | --- | --- |
| [Get Outdated Project Sdks](actions/getoutdatedprojectsdks.md) | GET | Retrieves outdated project SDKs from Unleash. |

### Get Outdated Sdks

| Action | Method | Description |
| --- | --- | --- |
| [Get Outdated Sdks](actions/getoutdatedsdks.md) | GET | Retrieves outdated SDKs from Unleash. |

### Get Project Role Mappings

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Role Mappings](actions/getroleprojectaccess.md) | GET | Retrieves project-role mappings from Unleash. |

### Get Public Signup Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Public Signup Tokens](actions/getallpublicsignuptokens.md) | GET | Retrieves public signup tokens from Unleash. |

### Get Release Plans.

| Action | Method | Description |
| --- | --- | --- |
| [Get Release Plans.](actions/getreleaseplans.md) | GET | Retrieves release plans from Unleash. |
| [Get Release Plans.](actions/oldgetreleaseplans.md) | GET |  |

### Get Roles For Currently Logged In User

| Action | Method | Description |
| --- | --- | --- |
| [Get Roles For Currently Logged In User](actions/getuserroles.md) | GET | Retrieves roles for currently logged in user from Unleash. |

### Get Saml Auth Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Saml Auth Settings](actions/getsamlsettings.md) | GET | Retrieves SAML auth settings from Unleash. |

### Get Scheduled Change Requests Matching A Query.

| Action | Method | Description |
| --- | --- | --- |
| [Get Scheduled Change Requests Matching A Query.](actions/getscheduledchangerequests.md) | GET | Retrieves scheduled change requests matching a query from Unleash. |

### Get Scim Settings.

| Action | Method | Description |
| --- | --- | --- |
| [Get Scim Settings.](actions/getscimsettings.md) | GET | Retrieves SCIM settings from Unleash. |

### Get Signup Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Signup Data](actions/getsignupdata.md) | GET | Retrieves signup data from Unleash. |

### Get Simple Auth Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Simple Auth Settings](actions/getsimplesettings.md) | GET | Retrieves Simple auth settings from Unleash. |

### Get Stored Custom Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Stored Custom Metrics](actions/getcustommetrics.md) | GET | Retrieves stored custom metrics from Unleash. |

### Get Strategies That Reference Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get Strategies That Reference Segment](actions/get-api-admin-segments-id-strategies.md) | GET | Retrieves strategies that reference segment from Unleash. |

### Get Strategies That Use A Context Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Strategies That Use A Context Field](actions/get-api-admin-context-contextfield-strategies.md) | GET | Retrieves strategies that use a context field from Unleash. |

### Get Strategy Segments

| Action | Method | Description |
| --- | --- | --- |
| [Get Strategy Segments](actions/get-api-admin-segments-strategies-strategyid.md) | GET | Retrieves strategy segments from Unleash. |

### Get Telemetry Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Telemetry Settings](actions/gettelemetrysettings.md) | GET | Retrieves telemetry settings from Unleash. |

### Get The Environment With `name`

| Action | Method | Description |
| --- | --- | --- |
| [Get The Environment With `Name`](actions/getenvironment.md) | GET | Retrieves the named environment from Unleash. |

### Get The Environments Available To A Project

| Action | Method | Description |
| --- | --- | --- |
| [Get The Environments Available To A Project](actions/getprojectenvironments.md) | GET | Retrieves the environments available to a project from Unleash. |

### Get The Most Recent Events From The Unleash Instance Or All Events Related To A

| Action | Method | Description |
| --- | --- | --- |
| [Get The Most Recent Events From The Unleash Instance Or All Events Related To A](actions/getevents.md) | GET | Retrieves recent instance or project events from Unleash. |

### Get The Number Of Change Requests You Can Do Something With

| Action | Method | Description |
| --- | --- | --- |
| [Get The Number Of Change Requests You Can Do Something With](actions/getactionablechangerequests.md) | GET | Retrieves the number of change requests you can do something with from Unleash. |

### Get Total Count Of Admin Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Total Count Of Admin Accounts](actions/getadmincount.md) | GET | Retrieves total count of admin accounts from Unleash. |

### Get Ui Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get Ui Configuration](actions/getuiconfig.md) | GET | Retrieves UI configuration from Unleash. |

### Get Unknown Flags

| Action | Method | Description |
| --- | --- | --- |
| [Get Unknown Flags](actions/getunknownflags.md) | GET | Retrieves unknown flags from Unleash. |

### Get User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/getuser.md) | GET | Retrieves user from Unleash. |

### Get Users And Groups In Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Users And Groups In Project](actions/getprojectaccess.md) | GET | Retrieves users and groups in project from Unleash. |

### Get Variants For A Feature In An Environment

| Action | Method | Description |
| --- | --- | --- |
| [Get Variants For A Feature In An Environment](actions/getenvironmentfeaturevariants.md) | GET | Retrieves variants for a feature in an environment from Unleash. |

### Get Your Own User Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Your Own User Details](actions/getme.md) | GET | Retrieves your own user details from Unleash. |

### Get Your Own User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Your Own User Profile](actions/getprofile.md) | GET | Retrieves your own user profile from Unleash. |

### Gets Access Overview

| Action | Method | Description |
| --- | --- | --- |
| [Gets Access Overview](actions/getaccessoverview.md) | GET | Retrieves access overview from Unleash. |

### Gets Available Permissions

| Action | Method | Description |
| --- | --- | --- |
| [Gets Available Permissions](actions/getpermissions.md) | GET | Retrieves available permissions from Unleash. |

### Gets Configured Context Fields

| Action | Method | Description |
| --- | --- | --- |
| [Gets Configured Context Fields](actions/getcontextfields.md) | GET | Retrieves configured context fields from Unleash. |

### Gets Context Field

| Action | Method | Description |
| --- | --- | --- |
| [Gets Context Field](actions/getcontextfield.md) | GET | Retrieves context field from Unleash. |

### Gets Inactive Users

| Action | Method | Description |
| --- | --- | --- |
| [Gets Inactive Users](actions/getinactiveusers.md) | GET | Retrieves inactive users from Unleash. |

### Gets Usage Data

| Action | Method | Description |
| --- | --- | --- |
| [Gets Usage Data](actions/getrequestspersecond.md) | GET | Retrieves usage data from Unleash. |

### Heartbeat For Enterprise Edge Instances.

| Action | Method | Description |
| --- | --- | --- |
| [Heartbeat For Enterprise Edge Instances.](actions/edgeinstanceheartbeat.md) | POST | Sends a heartbeat for Enterprise Edge instances in Unleash. |

### Import Feature Flags

| Action | Method | Description |
| --- | --- | --- |
| [Import Feature Flags](actions/post-api-admin-features-batch-import.md) | POST | Imports feature flags into Unleash. |

### Instance Usage Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Instance Usage Statistics](actions/getinstanceadminstats.md) | GET | Retrieves instance usage statistics from Unleash. |
| [Instance Usage Statistics](actions/getinstanceadminstatscsv.md) | GET | Retrieves instance usage statistics from Unleash. |

### Last Hour Of Usage And A List Of Applications That Have Reported Seeing This Fea

| Action | Method | Description |
| --- | --- | --- |
| [Last Hour Of Usage And A List Of Applications That Have Reported Seeing This Fea](actions/getfeatureusagesummary.md) | GET | Retrieves recent feature usage and reporting applications from Unleash. |

### List All Tags Of A Given Type.

| Action | Method | Description |
| --- | --- | --- |
| [List All Tags Of A Given Type.](actions/gettagsbytype.md) | GET | Retrieves all tags of a given type from Unleash. |

### List All Tags.

| Action | Method | Description |
| --- | --- | --- |
| [List All Tags.](actions/gettags.md) | GET | Retrieves all tags from Unleash. |

### List All Tokens For A Service Account.

| Action | Method | Description |
| --- | --- | --- |
| [List All Tokens For A Service Account.](actions/getserviceaccounttokens.md) | GET | Retrieves all tokens for a service account from Unleash. |

### List Parent Feature Variants.

| Action | Method | Description |
| --- | --- | --- |
| [List Parent Feature Variants.](actions/listparentvariantoptions.md) | GET | Retrieves parent feature variants from Unleash. |

### List Parent Options.

| Action | Method | Description |
| --- | --- | --- |
| [List Parent Options.](actions/listparentoptions.md) | GET | Retrieves parent options from Unleash. |

### List Service Accounts.

| Action | Method | Description |
| --- | --- | --- |
| [List Service Accounts.](actions/getserviceaccounts.md) | GET | Retrieves service accounts from Unleash. |

### Log In

| Action | Method | Description |
| --- | --- | --- |
| [Log In](actions/login.md) | POST | Logs in to Unleash. |

### Mark Features As Stale / Not Stale

| Action | Method | Description |
| --- | --- | --- |
| [Mark Features As Stale / Not Stale](actions/stalefeatures.md) | POST | Marks features as stale / not stale in Unleash. |

### Mark Notifications As Read

| Action | Method | Description |
| --- | --- | --- |
| [Mark Notifications As Read](actions/marknotificationsasread.md) | POST | Marks notifications as read in Unleash. |

### Modify A Feature Flag

| Action | Method | Description |
| --- | --- | --- |
| [Modify A Feature Flag](actions/patchfeature.md) | PUT | Updates a feature flag in Unleash. |

### Move Feature To Project

| Action | Method | Description |
| --- | --- | --- |
| [Move Feature To Project](actions/changeproject.md) | POST | Moves a feature to a project in Unleash. |

### Patch A Feature's Variants In An Environment

| Action | Method | Description |
| --- | --- | --- |
| [Patch A Feature's Variants In An Environment](actions/patchenvironmentsfeaturevariants.md) | PUT | Patches feature variants in an environment in Unleash. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get projects](actions/get-projects.md) | GET | Retrieves projects from Unleash. |

### Reactivate A Strategy

| Action | Method | Description |
| --- | --- | --- |
| [Reactivate A Strategy](actions/post-api-admin-strategies-strategyname-reactivate.md) | POST | Reactivates a strategy in Unleash. |

### Reads The Unleash License.

| Action | Method | Description |
| --- | --- | --- |
| [Reads The Unleash License.](actions/readlicense.md) | GET | Retrieves the license from Unleash. |

### Register A Client Sdk

| Action | Method | Description |
| --- | --- | --- |
| [Register A Client Sdk](actions/registerclientapplication.md) | POST | Registers a client SDK in Unleash. |
| [Register A Client Sdk](actions/registerfrontendclient.md) | POST | Registers a client SDK in Unleash. |

### Register Client Usage Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Register Client Usage Metrics](actions/registerclientmetrics.md) | POST | Registers a client usage metrics in Unleash. |
| [Register Client Usage Metrics](actions/registerfrontendmetrics.md) | POST | Registers a client usage metrics in Unleash. |

### Register Edge Observability Metrics.

| Action | Method | Description |
| --- | --- | --- |
| [Register Edge Observability Metrics.](actions/registeredgeobservabilitymetrics.md) | POST | Registers an Edge observability metrics in Unleash. |

### Reject A User Access Request.

| Action | Method | Description |
| --- | --- | --- |
| [Reject A User Access Request.](actions/rejectuseraccessrequest.md) | DELETE | Rejects a user access request in Unleash. |

### Remove A Release Plan.

| Action | Method | Description |
| --- | --- | --- |
| [Remove A Release Plan.](actions/oldremovereleaseplan.md) | DELETE |  |
| [Remove A Release Plan.](actions/removereleaseplan.md) | DELETE | Removes a release plan from Unleash. |

### Remove An Environment From A Project.

| Action | Method | Description |
| --- | --- | --- |
| [Remove An Environment From A Project.](actions/removeenvironmentfromproject.md) | DELETE | Removes an environment from a project from Unleash. |

### Remove Feature From Favorites

| Action | Method | Description |
| --- | --- | --- |
| [Remove Feature From Favorites](actions/removefavoritefeature.md) | DELETE | Removes a feature from favorites from Unleash. |

### Remove Project Access For A Group

| Action | Method | Description |
| --- | --- | --- |
| [Remove Project Access For A Group](actions/removegroupaccess.md) | DELETE | Removes project access for a group from Unleash. |

### Remove Project Access For A User

| Action | Method | Description |
| --- | --- | --- |
| [Remove Project Access For A User](actions/removeuseraccess.md) | DELETE | Removes project access for a user from Unleash. |

### Remove Project From Favorites

| Action | Method | Description |
| --- | --- | --- |
| [Remove Project From Favorites](actions/removefavoriteproject.md) | DELETE | Removes a project from favorites from Unleash. |

### Removes A Strategy Attached To A Milestone

| Action | Method | Description |
| --- | --- | --- |
| [Removes A Strategy Attached To A Milestone](actions/delete-api-admin-release-plan-templates-templateid-milestones-milestoneid-strategies-strat.md) | DELETE | Removes a strategy attached to a milestone from Unleash. |

### Removes A Tag From A Feature.

| Action | Method | Description |
| --- | --- | --- |
| [Removes A Tag From A Feature.](actions/delete-api-admin-features-featurename-tags-type-value.md) | DELETE | Removes a tag from a feature from Unleash. |

### Removes An Existing Milestone

| Action | Method | Description |
| --- | --- | --- |
| [Removes An Existing Milestone](actions/removereleasetemplatemilestone.md) | DELETE | Removes an existing milestone from Unleash. |

### Reset Password

| Action | Method | Description |
| --- | --- | --- |
| [Reset Password](actions/sendresetpasswordemail.md) | POST | Sends a password reset email from Unleash. |

### Reset User Password

| Action | Method | Description |
| --- | --- | --- |
| [Reset User Password](actions/resetuserpassword.md) | POST | Resets a user's password in Unleash. |

### Retrieve A Token

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve A Token](actions/getpublicsignuptoken.md) | GET | Retrieves a token from Unleash. |

### Retrieve Enabled Feature Flags For The Provided Context, Using Post.

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Enabled Feature Flags For The Provided Context, Using Post.](actions/getfrontendapifeatureswithpost.md) | POST | Retrieves enabled feature flags for the provided context from Unleash using POST. |

### Retrieve Enabled Feature Flags For The Provided Context.

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Enabled Feature Flags For The Provided Context.](actions/getfrontendfeatures.md) | GET | Retrieves enabled feature flags for the provided context from Unleash. |

### Retrieves A List Of Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Retrieves A List Of Notifications](actions/getnotifications.md) | GET | Retrieves a list of notifications from Unleash. |

### Retrieves All Change Requests For A Project

| Action | Method | Description |
| --- | --- | --- |
| [Retrieves All Change Requests For A Project](actions/getchangerequestsforproject.md) | GET | Retrieves all change requests for a project from Unleash. |

### Retrieves All Licensed Users Data.

| Action | Method | Description |
| --- | --- | --- |
| [Retrieves All Licensed Users Data.](actions/getalllicensedusers.md) | GET | Retrieves all licensed users data from Unleash. |

### Retrieves All Pending Change Requests Referencing A Feature In The Project

| Action | Method | Description |
| --- | --- | --- |
| [Retrieves All Pending Change Requests Referencing A Feature In The Project](actions/getpendingchangerequestsforfeature.md) | GET | Retrieves all pending change requests referencing a feature in the project from Unleash. |

### Retrieves Change Request Configuration For A Project

| Action | Method | Description |
| --- | --- | --- |
| [Retrieves Change Request Configuration For A Project](actions/getprojectchangerequestconfig.md) | GET | Retrieves change request configuration for a project from Unleash. |

### Retrieves Number Of Project Change Requests In Each State

| Action | Method | Description |
| --- | --- | --- |
| [Retrieves Number Of Project Change Requests In Each State](actions/getchangerequestscount.md) | GET | Retrieves number of project change requests in each state from Unleash. |

### Retrieves One Change Request By Id

| Action | Method | Description |
| --- | --- | --- |
| [Retrieves One Change Request By Id](actions/getchangerequest.md) | GET | Retrieves one change request by id from Unleash. |

### Retrieves Pending Change Requests In Configured Environments

| Action | Method | Description |
| --- | --- | --- |
| [Retrieves Pending Change Requests In Configured Environments](actions/getopenchangerequestsforuser.md) | GET |  |
| [Retrieves Pending Change Requests In Configured Environments](actions/getpendingchangerequestsforuser.md) | GET | Retrieves pending change requests in configured environments from Unleash. |

### Returns The List Of Permissions For The Service Account.

| Action | Method | Description |
| --- | --- | --- |
| [Returns The List Of Permissions For The Service Account.](actions/getserviceaccountpermissions.md) | GET | Retrieves the list of permissions for the service account from Unleash. |

### Revive Project

| Action | Method | Description |
| --- | --- | --- |
| [Revive Project](actions/reviveproject.md) | POST | Revives a project in Unleash. |

### Revives A Feature

| Action | Method | Description |
| --- | --- | --- |
| [Revives A Feature](actions/revivefeature.md) | POST | Revives a feature in Unleash. |

### Revives A List Of Features

| Action | Method | Description |
| --- | --- | --- |
| [Revives A List Of Features](actions/revivefeatures.md) | POST | Revives a list of features in Unleash. |

### Search And Filter Features

| Action | Method | Description |
| --- | --- | --- |
| [Search And Filter Features](actions/get-api-admin-search-features.md) | GET | Searches and filter features in Unleash. |

### Search For Events

| Action | Method | Description |
| --- | --- | --- |
| [Search For Events](actions/searchevents.md) | GET | Searches for events in Unleash. |

### Search Users

| Action | Method | Description |
| --- | --- | --- |
| [Search Users](actions/searchusers.md) | GET | Searches users in Unleash. |

### Send Custom Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Send Custom Metrics](actions/clientcustommetrics.md) | POST | Sends custom metrics in Unleash. |

### Send Metrics In Bulk

| Action | Method | Description |
| --- | --- | --- |
| [Send Metrics In Bulk](actions/clientbulkmetrics.md) | POST | Sends metrics in bulk in Unleash. |

### Send Unleash Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Send Unleash Feedback](actions/createfeedback.md) | POST | Sends feedback in Unleash. |

### Set A New Unleash License.

| Action | Method | Description |
| --- | --- | --- |
| [Set A New Unleash License.](actions/updatelicense.md) | POST | Sets a new license in Unleash. |

### Set Environment Default Strategy

| Action | Method | Description |
| --- | --- | --- |
| [Set Environment Default Strategy](actions/adddefaultstrategytoprojectenvironment.md) | POST | Sets environment-default strategy in Unleash. |

### Set Oidc Settings

| Action | Method | Description |
| --- | --- | --- |
| [Set Oidc Settings](actions/setoidcsettings.md) | POST | Sets OIDC settings in Unleash. |

### Set Scim Settings.

| Action | Method | Description |
| --- | --- | --- |
| [Set Scim Settings.](actions/setscimsettings.md) | POST | Sets SCIM settings in Unleash. |

### Set Strategy Sort Order

| Action | Method | Description |
| --- | --- | --- |
| [Set Strategy Sort Order](actions/setstrategysortorder.md) | POST | Sets strategy sort order in Unleash. |

### Set Users And Groups To Roles In The Current Project

| Action | Method | Description |
| --- | --- | --- |
| [Set Users And Groups To Roles In The Current Project](actions/setprojectaccess.md) | PUT | Sets users and groups to roles in the current project in Unleash. |

### Sets Allowed Cors Origins

| Action | Method | Description |
| --- | --- | --- |
| [Sets Allowed Cors Origins](actions/setcors.md) | POST | Sets allowed CORS origins in Unleash. |

### Sets Roles For Group

| Action | Method | Description |
| --- | --- | --- |
| [Sets Roles For Group](actions/setrolesforgroup.md) | PUT | Sets roles for group in Unleash. |

### Sets Roles For User

| Action | Method | Description |
| --- | --- | --- |
| [Sets Roles For User](actions/setrolesforuser.md) | PUT | Sets roles for user in Unleash. |

### Start A Release Plan Milestone.

| Action | Method | Description |
| --- | --- | --- |
| [Start A Release Plan Milestone.](actions/oldstartmilestone.md) | POST |  |
| [Start A Release Plan Milestone.](actions/startmilestone.md) | POST | Starts a release plan milestone in Unleash. |

### Submit Signup Data.

| Action | Method | Description |
| --- | --- | --- |
| [Submit Signup Data.](actions/submitsignupdata.md) | POST | Submits signup data to Unleash. |

### This Endpoint Fetches The Requested Approvers Of A Change Request

| Action | Method | Description |
| --- | --- | --- |
| [This Endpoint Fetches The Requested Approvers Of A Change Request](actions/getchangerequestapprovers.md) | GET | Retrieves change request approvers from Unleash. |

### This Endpoint Will Add A Comment To A Change Request

| Action | Method | Description |
| --- | --- | --- |
| [This Endpoint Will Add A Comment To A Change Request](actions/addchangerequestcomment.md) | POST | Adds a comment to a change request in Unleash. |

### This Endpoint Will Return Users Available To Review/approve This Change Request

| Action | Method | Description |
| --- | --- | --- |
| [This Endpoint Will Return Users Available To Review/Approve This Change Request](actions/getavailablechangerequestreviewers.md) | GET | Retrieves available change request reviewers from Unleash. |

### This Endpoint Will Update The Custom Title Of A Change Request

| Action | Method | Description |
| --- | --- | --- |
| [This Endpoint Will Update The Custom Title Of A Change Request](actions/updatechangerequesttitle.md) | PUT | Updates a change request title in Unleash. |

### This Endpoint Will Update The Reviewers Of A Change Request

| Action | Method | Description |
| --- | --- | --- |
| [This Endpoint Will Update The Reviewers Of A Change Request](actions/addchangerequestreviewers.md) | PUT | Updates change request reviewers in Unleash. |

### This Endpoint Will Update The State Of A Change Request

| Action | Method | Description |
| --- | --- | --- |
| [This Endpoint Will Update The State Of A Change Request](actions/updatechangerequeststate.md) | PUT | Updates a change request state in Unleash. |

### Toggle The Environment With `name` Off

| Action | Method | Description |
| --- | --- | --- |
| [Toggle The Environment With `Name` Off](actions/toggleenvironmentoff.md) | POST | Disables the named environment in Unleash. |

### Toggle The Environment With `name` On

| Action | Method | Description |
| --- | --- | --- |
| [Toggle The Environment With `Name` On](actions/toggleenvironmenton.md) | POST | Enables the named environment in Unleash. |

### Update A Banner.

| Action | Method | Description |
| --- | --- | --- |
| [Update A Banner.](actions/updatebanner.md) | PUT | Updates a banner in Unleash. |

### Update A Feature Flag

| Action | Method | Description |
| --- | --- | --- |
| [Update A Feature Flag](actions/updatefeature.md) | PUT | Updates a feature flag in Unleash. |

### Update A Group

| Action | Method | Description |
| --- | --- | --- |
| [Update A Group](actions/updategroup.md) | PUT | Updates a group in Unleash. |

### Update A Public Signup Token

| Action | Method | Description |
| --- | --- | --- |
| [Update A Public Signup Token](actions/updatepublicsignuptoken.md) | PUT | Updates a public signup token in Unleash. |

### Update A Role

| Action | Method | Description |
| --- | --- | --- |
| [Update A Role](actions/updaterole.md) | PUT | Updates a role in Unleash. |

### Update A Service Account.

| Action | Method | Description |
| --- | --- | --- |
| [Update A Service Account.](actions/updateserviceaccount.md) | PUT | Updates a service account in Unleash. |

### Update A Strategy

| Action | Method | Description |
| --- | --- | --- |
| [Update A Strategy](actions/updatefeaturestrategy.md) | PUT | Updates a strategy in Unleash. |

### Update A Strategy Type

| Action | Method | Description |
| --- | --- | --- |
| [Update A Strategy Type](actions/put-api-admin-strategies-name.md) | PUT | Updates a strategy type in Unleash. |

### Update A Tag Type

| Action | Method | Description |
| --- | --- | --- |
| [Update A Tag Type](actions/updatetagtype.md) | PUT | Updates a tag type in Unleash. |

### Update A User

| Action | Method | Description |
| --- | --- | --- |
| [Update A User](actions/updateuser.md) | PUT | Updates a user in Unleash. |

### Update An Addon

| Action | Method | Description |
| --- | --- | --- |
| [Update An Addon](actions/updateaddon.md) | PUT | Updates an addon in Unleash. |

### Update An Existing Context Field

| Action | Method | Description |
| --- | --- | --- |
| [Update An Existing Context Field](actions/updatecontextfield.md) | PUT | Updates an existing context field in Unleash. |

### Update Api Token

| Action | Method | Description |
| --- | --- | --- |
| [Update Api Token](actions/updateapitoken.md) | PUT | Updates an API token in Unleash. |

### Update Environment Sort Orders

| Action | Method | Description |
| --- | --- | --- |
| [Update Environment Sort Orders](actions/updatesortorder.md) | PUT | Updates an environment sort orders in Unleash. |

### Update Feature Type Lifetime

| Action | Method | Description |
| --- | --- | --- |
| [Update Feature Type Lifetime](actions/put-api-admin-feature-types-id-lifetime.md) | PUT | Updates a feature type lifetime in Unleash. |

### Update Project

| Action | Method | Description |
| --- | --- | --- |
| [Update Project](actions/updateproject.md) | PUT | Updates a project in Unleash. |

### Update Project Enterprise Settings

| Action | Method | Description |
| --- | --- | --- |
| [Update Project Enterprise Settings](actions/updateprojectenterprisesettings.md) | PUT | Updates a project enterprise settings in Unleash. |

### Update Saml Auth Settings

| Action | Method | Description |
| --- | --- | --- |
| [Update Saml Auth Settings](actions/setsamlsettings.md) | POST | Updates a SAML auth settings in Unleash. |

### Update Segment By Id

| Action | Method | Description |
| --- | --- | --- |
| [Update Segment By Id](actions/updatesegment.md) | PUT | Updates a segment by id in Unleash. |

### Update Simple Auth Settings

| Action | Method | Description |
| --- | --- | --- |
| [Update Simple Auth Settings](actions/setsimplesettings.md) | POST | Updates a Simple auth settings in Unleash. |

### Update Splash Settings

| Action | Method | Description |
| --- | --- | --- |
| [Update Splash Settings](actions/updatesplashsettings.md) | POST | Updates a splash settings in Unleash. |

### Update Strategy Segments

| Action | Method | Description |
| --- | --- | --- |
| [Update Strategy Segments](actions/post-api-admin-segments-strategies.md) | POST | Updates a strategy segments in Unleash. |

### Update Unleash Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Update Unleash Feedback](actions/updatefeedback.md) | PUT | Updates feedback in Unleash. |

### Updates A Release Template By Its Id.

| Action | Method | Description |
| --- | --- | --- |
| [Updates A Release Template By Its Id.](actions/updatereleasetemplate.md) | PUT | Updates a release template by its id in Unleash. |

### Updates A Strategy Attached To A Milestone

| Action | Method | Description |
| --- | --- | --- |
| [Updates A Strategy Attached To A Milestone](actions/put-api-admin-release-plan-templates-templateid-milestones-milestoneid-strategies-strategy.md) | PUT | Updates a strategy attached to a milestone in Unleash. |

### Updates An Environment By Name

| Action | Method | Description |
| --- | --- | --- |
| [Updates An Environment By Name](actions/updateenvironment.md) | PUT | Updates an environment by name in Unleash. |

### Updates Change Request Configuration For An Environment In The Project

| Action | Method | Description |
| --- | --- | --- |
| [Updates Change Request Configuration For An Environment In The Project](actions/updateprojectchangerequestconfig.md) | PUT | Updates change request configuration for an environment in the project in Unleash. |

### Updates Existing Milestone

| Action | Method | Description |
| --- | --- | --- |
| [Updates Existing Milestone](actions/updatereleasetemplatemilestone.md) | PUT | Updates an existing milestone in Unleash. |

### Updates Multiple Tags For A Feature.

| Action | Method | Description |
| --- | --- | --- |
| [Updates Multiple Tags For A Feature.](actions/put-api-admin-features-featurename-tags.md) | PUT | Updates multiple tags for a feature in Unleash. |

### Validate A Context Field

| Action | Method | Description |
| --- | --- | --- |
| [Validate A Context Field](actions/validatecontextfieldname.md) | POST | Validates a context field in Unleash. |

### Validate A Feature Flag Name.

| Action | Method | Description |
| --- | --- | --- |
| [Validate A Feature Flag Name.](actions/post-api-admin-features-validate.md) | POST | Validates a feature flag name in Unleash. |

### Validate A Role

| Action | Method | Description |
| --- | --- | --- |
| [Validate A Role](actions/validaterole.md) | POST | Validates a role in Unleash. |

### Validate A Tag Type

| Action | Method | Description |
| --- | --- | --- |
| [Validate A Tag Type](actions/validatetagtype.md) | POST | Validates a tag type in Unleash. |

### Validate Constraint

| Action | Method | Description |
| --- | --- | --- |
| [Validate Constraint](actions/validateconstraint.md) | POST | Validates a constraint in Unleash. |

### Validate Feature Import Data

| Action | Method | Description |
| --- | --- | --- |
| [Validate Feature Import Data](actions/post-api-admin-features-batch-validate.md) | POST | Validates a feature import data in Unleash. |

### Validate Password For A User

| Action | Method | Description |
| --- | --- | --- |
| [Validate Password For A User](actions/validateuserpassword.md) | POST | Validates password for a user in Unleash. |

### Validate Project Id

| Action | Method | Description |
| --- | --- | --- |
| [Validate Project Id](actions/validateproject.md) | POST | Validates a project ID in Unleash. |

### Validate Signup Token

| Action | Method | Description |
| --- | --- | --- |
| [Validate Signup Token](actions/validatepublicsignuptoken.md) | GET | Validates signup token in Unleash. |

### Validates A Token

| Action | Method | Description |
| --- | --- | --- |
| [Validates A Token](actions/validatetoken.md) | GET | Validates a token in Unleash. |

### Validates Archive Features

| Action | Method | Description |
| --- | --- | --- |
| [Validates Archive Features](actions/validatearchivefeatures.md) | POST | Validates an archive features in Unleash. |

### Validates If A Segment Name Exists

| Action | Method | Description |
| --- | --- | --- |
| [Validates If A Segment Name Exists](actions/validatesegment.md) | POST | Validates if a segment name exists in Unleash. |

### Validates If An Environment Name Exists

| Action | Method | Description |
| --- | --- | --- |
| [Validates If An Environment Name Exists](actions/validateenvironmentname.md) | POST | Validates if an environment name exists in Unleash. |

### Validates Password

| Action | Method | Description |
| --- | --- | --- |
| [Validates Password](actions/validatepassword.md) | POST | Validates a password in Unleash. |

### Validates The Unleash License.

| Action | Method | Description |
| --- | --- | --- |
| [Validates The Unleash License.](actions/checklicense.md) | GET | Validates the license in Unleash. |

