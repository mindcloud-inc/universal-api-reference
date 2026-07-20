# Unleash: Native API Reference

A consolidated summary of Unleash's API configuration and 376 documented operations, with links to official documentation.

- **Official docs:** https://docs.getunleash.io/api
- **OpenAPI specification:** https://us.app.getunleash.io/uspp0456/docs/openapi.json
- **API base URL:** `https://us.app.getunleash.io/uspp0456`

## Authentication

### API Key

Use an Unleash API token or service account token. Requests are authenticated with the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.getunleash.io/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–200). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (376 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Configure Project Access](actions/addaccesstoproject.md) | `POST /api/admin/projects/{projectId}/access` | [docs](https://docs.getunleash.io/api) |
| [This Endpoint Will Add A Comment To A Change Request](actions/addchangerequestcomment.md) | `POST /api/admin/projects/{projectId}/change-requests/{id}/comments` | [docs](https://docs.getunleash.io/api) |
| [This Endpoint Will Update The Reviewers Of A Change Request](actions/addchangerequestreviewers.md) | `PUT /api/admin/projects/{projectId}/change-requests/{id}/approvers` | [docs](https://docs.getunleash.io/api) |
| [Set Environment Default Strategy](actions/adddefaultstrategytoprojectenvironment.md) | `POST /api/admin/projects/{projectId}/environments/{environment}/default-strategy` | [docs](https://docs.getunleash.io/api) |
| [Add An Environment To A Project.](actions/addenvironmenttoproject.md) | `POST /api/admin/projects/{projectId}/environments` | [docs](https://docs.getunleash.io/api) |
| [Add Feature To Favorites](actions/addfavoritefeature.md) | `POST /api/admin/projects/{projectId}/features/{featureName}/favorites` | [docs](https://docs.getunleash.io/api) |
| [Add Project To Favorites](actions/addfavoriteproject.md) | `POST /api/admin/projects/{projectId}/favorites` | [docs](https://docs.getunleash.io/api) |
| [Add A Feature Dependency.](actions/addfeaturedependency.md) | `POST /api/admin/projects/{projectId}/features/{child}/dependencies` | [docs](https://docs.getunleash.io/api) |
| [Add A Strategy To A Feature Flag](actions/addfeaturestrategy.md) | `POST /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies` | [docs](https://docs.getunleash.io/api) |
| [Adds A Milestone To A Release Template.](actions/addmilestonetoreleasetemplate.md) | `POST /api/admin/release-plan-templates/{templateId}/milestones` | [docs](https://docs.getunleash.io/api) |
| [Add A User Via A Signup Token](actions/addpublicsignuptokenuser.md) | `POST /invite/{token}/signup` | [docs](https://docs.getunleash.io/api) |
| [Add A Release Plan.](actions/addreleaseplan.md) | `POST /api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans` | [docs](https://docs.getunleash.io/api) |
| [Adds A Tag To The Specified Features](actions/addtagtofeatures.md) | `PUT /api/admin/projects/{projectId}/tags` | [docs](https://docs.getunleash.io/api) |
| [Approve A User Access Request.](actions/approveuseraccessrequest.md) | `POST /api/admin/user-access-requests/{id}/approve` | [docs](https://docs.getunleash.io/api) |
| [Archive A Feature Flag](actions/archivefeature.md) | `DELETE /api/admin/projects/{projectId}/features/{featureName}` | [docs](https://docs.getunleash.io/api) |
| [Archives A List Of Features](actions/archivefeatures.md) | `POST /api/admin/projects/{projectId}/archive` | [docs](https://docs.getunleash.io/api) |
| [Archive Project](actions/archiveproject.md) | `POST /api/admin/projects/archive/{projectId}` | [docs](https://docs.getunleash.io/api) |
| [Archives A Release Template By Its Id.](actions/archivereleasetemplate.md) | `POST /api/admin/release-plan-templates/archive/{templateId}` | [docs](https://docs.getunleash.io/api) |
| [Bulk Disable A List Of Features](actions/bulktogglefeaturesenvironmentoff.md) | `POST /api/admin/projects/{projectId}/bulk_features/environments/{environment}/off` | [docs](https://docs.getunleash.io/api) |
| [Bulk Enable A List Of Features](actions/bulktogglefeaturesenvironmenton.md) | `POST /api/admin/projects/{projectId}/bulk_features/environments/{environment}/on` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Call A Signal Endpoint.](actions/callsignalendpoint.md) | `POST /api/signal-endpoint/{name}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Change A Feature Environment Safeguard](actions/changefeatureenvsafeguard.md) | `PUT /api/admin/projects/{project}/features/{featureName}/environments/{environment}/safeguards` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Create Or Update A Milestone Progression](actions/changemilestoneprogression.md) | `PUT /api/admin/projects/{project}/features/{featureName}/environments/{environment}/progressions/{id}` | [docs](https://docs.getunleash.io/api) |
| [Change Your Own Password](actions/changemypassword.md) | `POST /api/admin/user/change-password` | [docs](https://docs.getunleash.io/api) |
| [Changes A User Password](actions/changepassword.md) | `POST /auth/reset/password` | [docs](https://docs.getunleash.io/api) |
| [Move Feature To Project](actions/changeproject.md) | `POST /api/admin/projects/{projectId}/features/{featureName}/changeProject` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Change A Release Plan Safeguard](actions/changereleaseplansafeguard.md) | `PUT /api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans/{planId}/safeguards` | [docs](https://docs.getunleash.io/api) |
| [Create/Add Change To A Change Request](actions/changerequest.md) | `POST /api/admin/projects/{projectId}/environments/{environment}/change-requests` | [docs](https://docs.getunleash.io/api) |
| [Change Password For A User](actions/changeuserpassword.md) | `POST /api/admin/user-admin/{id}/change-password` | [docs](https://docs.getunleash.io/api) |
| [Check Dependencies Exist.](actions/checkdependenciesexist.md) | `GET /api/admin/projects/{projectId}/dependencies` | [docs](https://docs.getunleash.io/api) |
| [Validates The Unleash License.](actions/checklicense.md) | `GET /api/admin/license/check` | [docs](https://docs.getunleash.io/api) |
| [Send Metrics In Bulk](actions/clientbulkmetrics.md) | `POST /api/client/metrics/bulk` | [docs](https://docs.getunleash.io/api) |
| [Send Custom Metrics](actions/clientcustommetrics.md) | `POST /api/client/metrics/custom` | [docs](https://docs.getunleash.io/api) |
| [Clones An Environment](actions/cloneenvironment.md) | `POST /api/admin/environments/{name}/clone` | [docs](https://docs.getunleash.io/api) |
| [Clone A Feature Flag](actions/clonefeature.md) | `POST /api/admin/projects/{projectId}/features/{featureName}/clone` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Set Feature Completed](actions/complete.md) | `POST /api/admin/projects/{projectId}/features/{featureName}/lifecycle/complete` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Connect To The Streaming Api.](actions/connect.md) | `GET /api/client/streaming` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Create An Action Set.](actions/createactions.md) | `POST /api/admin/projects/{projectId}/actions` | [docs](https://docs.getunleash.io/api) |
| [Create A New Addon](actions/createaddon.md) | `POST /api/admin/addons` | [docs](https://docs.getunleash.io/api) |
| [Create Api Token](actions/createapitoken.md) | `POST /api/admin/api-tokens` | [docs](https://docs.getunleash.io/api) |
| [Create An Application To Connect Reported Metrics](actions/createapplication.md) | `POST /api/admin/metrics/applications/{appName}` | [docs](https://docs.getunleash.io/api) |
| [Create A Banner.](actions/createbanner.md) | `POST /api/admin/banners` | [docs](https://docs.getunleash.io/api) |
| [Create A Context Field](actions/createcontextfield.md) | `POST /api/admin/context` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Create A Context Field](actions/createcontextfieldforproject.md) | `POST /api/admin/projects/{projectId}/context` | [docs](https://docs.getunleash.io/api) |
| [Creates A New Environment](actions/createenvironment.md) | `POST /api/admin/environments` | [docs](https://docs.getunleash.io/api) |
| [Add A New Feature Flag](actions/createfeature.md) | `POST /api/admin/projects/{projectId}/features` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Create A Feature Link](actions/createfeaturelink.md) | `POST /api/admin/projects/{projectId}/features/{featureName}/link` | [docs](https://docs.getunleash.io/api) |
| [Send Unleash Feedback](actions/createfeedback.md) | `POST /api/admin/feedback` | [docs](https://docs.getunleash.io/api) |
| [Create A New Group](actions/creategroup.md) | `POST /api/admin/groups` | [docs](https://docs.getunleash.io/api) |
| [Create A New Personal Access Token (Pat) For The Current User.](actions/createpat.md) | `POST /api/admin/user/tokens` | [docs](https://docs.getunleash.io/api) |
| [Create Project](actions/createproject.md) | `POST /api/admin/projects` | [docs](https://docs.getunleash.io/api) |
| [Create A Project Api Token.](actions/createprojectapitoken.md) | `POST /api/admin/projects/{projectId}/api-tokens` | [docs](https://docs.getunleash.io/api) |
| [Create A Public Signup Token](actions/createpublicsignuptoken.md) | `POST /api/admin/invite-link/tokens` | [docs](https://docs.getunleash.io/api) |
| [Create A Release Template.](actions/createreleasetemplate.md) | `POST /api/admin/release-plan-templates` | [docs](https://docs.getunleash.io/api) |
| [Create A New Role](actions/createrole.md) | `POST /api/admin/roles` | [docs](https://docs.getunleash.io/api) |
| [Create A New Segment](actions/createsegment.md) | `POST /api/admin/segments` | [docs](https://docs.getunleash.io/api) |
| [Create A Service Account.](actions/createserviceaccount.md) | `POST /api/admin/service-account` | [docs](https://docs.getunleash.io/api) |
| [Create A Token For A Service Account.](actions/createserviceaccounttoken.md) | `POST /api/admin/service-account/{id}/token` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Create A Signal Endpoint.](actions/createsignalendpoint.md) | `POST /api/admin/signal-endpoints` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Create A Signal Endpoint Token For A Specific Signal Endpoint.](actions/createsignalendpointtoken.md) | `POST /api/admin/signal-endpoints/{signalEndpointId}/tokens` | [docs](https://docs.getunleash.io/api) |
| [Create A New Tag.](actions/createtag.md) | `POST /api/admin/tags` | [docs](https://docs.getunleash.io/api) |
| [Create A Tag Type](actions/createtagtype.md) | `POST /api/admin/tag-types` | [docs](https://docs.getunleash.io/api) |
| [Create A New User](actions/createuser.md) | `POST /api/admin/user-admin` | [docs](https://docs.getunleash.io/api) |
| [Removes A Tag From A Feature.](actions/delete-api-admin-features-featurename-tags-type-value.md) | `DELETE /api/admin/features/{featureName}/tags/{type}/{value}` | [docs](https://docs.getunleash.io/api) |
| [Removes A Strategy Attached To A Milestone](actions/delete-api-admin-release-plan-templates-templateid-milestones-milestoneid-strategies-strat.md) | `DELETE /api/admin/release-plan-templates/{templateId}/milestones/{milestoneId}/strategies/{strategyId}` | [docs](https://docs.getunleash.io/api) |
| [Delete A Strategy](actions/delete-api-admin-strategies-name.md) | `DELETE /api/admin/strategies/{name}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Delete An Action Set.](actions/deleteactions.md) | `DELETE /api/admin/projects/{projectId}/actions/{id}` | [docs](https://docs.getunleash.io/api) |
| [Delete An Addon](actions/deleteaddon.md) | `DELETE /api/admin/addons/{id}` | [docs](https://docs.getunleash.io/api) |
| [Delete Api Token](actions/deleteapitoken.md) | `DELETE /api/admin/api-tokens/{token}` | [docs](https://docs.getunleash.io/api) |
| [Delete An Application](actions/deleteapplication.md) | `DELETE /api/admin/metrics/applications/{appName}` | [docs](https://docs.getunleash.io/api) |
| [Delete A Banner.](actions/deletebanner.md) | `DELETE /api/admin/banners/{id}` | [docs](https://docs.getunleash.io/api) |
| [Discards A Change From A Change Request By Change Id](actions/deletechange.md) | `DELETE /api/admin/projects/{projectId}/change-requests/{changeRequestId}/changes/{changeId}` | [docs](https://docs.getunleash.io/api) |
| [Deletes A Change Request By Id](actions/deletechangerequest.md) | `DELETE /api/admin/projects/{projectId}/change-requests/{id}` | [docs](https://docs.getunleash.io/api) |
| [Delete An Existing Context Field](actions/deletecontextfield.md) | `DELETE /api/admin/context/{contextField}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Delete An Existing Context Field](actions/deletecontextfieldforproject.md) | `DELETE /api/admin/projects/{projectId}/context/{contextField}` | [docs](https://docs.getunleash.io/api) |
| [Delete Legal Value For The Context Field](actions/deletecontextfieldlegalvalue.md) | `DELETE /api/admin/context/{contextField}/legal-values/{legalValue}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Delete Legal Value For The Context Field](actions/deletecontextfieldlegalvalueforproject.md) | `DELETE /api/admin/projects/{projectId}/context/{contextField}/legal-values/{legalValue}` | [docs](https://docs.getunleash.io/api) |
| [Archives A Feature](actions/deletefeature.md) | `DELETE /api/admin/archive/{featureName}` | [docs](https://docs.getunleash.io/api) |
| [Deletes Feature Dependencies.](actions/deletefeaturedependencies.md) | `DELETE /api/admin/projects/{projectId}/features/{child}/dependencies` | [docs](https://docs.getunleash.io/api) |
| [Deletes A Feature Dependency.](actions/deletefeaturedependency.md) | `DELETE /api/admin/projects/{projectId}/features/{child}/dependencies/{parent}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Delete A Feature Environment Safeguard](actions/deletefeatureenvsafeguard.md) | `DELETE /api/admin/projects/{project}/features/{featureName}/environments/{environment}/safeguards/{safeguardId}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Delete A Feature Link](actions/deletefeaturelink.md) | `DELETE /api/admin/projects/{projectId}/features/{featureName}/link/{linkId}` | [docs](https://docs.getunleash.io/api) |
| [Deletes A List Of Features](actions/deletefeatures.md) | `POST /api/admin/projects/{projectId}/delete` | [docs](https://docs.getunleash.io/api) |
| [Delete A Strategy From A Feature Flag](actions/deletefeaturestrategy.md) | `DELETE /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies/{strategyId}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Delete Flag Level Impact Metric Configuration](actions/deleteflagimpactmetricconfig.md) | `DELETE /api/admin/projects/{projectId}/features/{featureName}/impact-metrics/config/{id}` | [docs](https://docs.getunleash.io/api) |
| [Delete A Single Group](actions/deletegroup.md) | `DELETE /api/admin/groups/{groupId}` | [docs](https://docs.getunleash.io/api) |
| [Deletes Inactive Users](actions/deleteinactiveusers.md) | `POST /api/admin/user-admin/inactive/delete` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Delete Instance Level Impact Metric Configuration](actions/deleteinstanceimpactmetricconfig.md) | `DELETE /api/admin/impact-metrics/config/{id}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Delete A Milestone Progression](actions/deletemilestoneprogression.md) | `DELETE /api/admin/projects/{project}/features/{featureName}/environments/{environment}/progressions/{id}` | [docs](https://docs.getunleash.io/api) |
| [Delete A Personal Access Token (Pat) For The Current User.](actions/deletepat.md) | `DELETE /api/admin/user/tokens/{id}` | [docs](https://docs.getunleash.io/api) |
| [Delete Project](actions/deleteproject.md) | `DELETE /api/admin/projects/{projectId}` | [docs](https://docs.getunleash.io/api) |
| [Delete A Project Api Token.](actions/deleteprojectapitoken.md) | `DELETE /api/admin/projects/{projectId}/api-tokens/{token}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Delete A Release Plan Safeguard](actions/deletereleaseplansafeguard.md) | `DELETE /api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans/{planId}/safeguards/{safeguardId}` | [docs](https://docs.getunleash.io/api) |
| [Deletes A Release Template By Its Id.](actions/deletereleasetemplate.md) | `DELETE /api/admin/release-plan-templates/{templateId}` | [docs](https://docs.getunleash.io/api) |
| [Delete A Custom Role](actions/deleterole.md) | `DELETE /api/admin/roles/{roleId}` | [docs](https://docs.getunleash.io/api) |
| [Delete All Scim Groups](actions/deletescimgroups.md) | `DELETE /api/admin/groups/scim-groups` | [docs](https://docs.getunleash.io/api) |
| [Delete All Scim Users](actions/deletescimusers.md) | `DELETE /api/admin/user-admin/scim-users` | [docs](https://docs.getunleash.io/api) |
| [Delete A Service Account.](actions/deleteserviceaccount.md) | `DELETE /api/admin/service-account/{id}` | [docs](https://docs.getunleash.io/api) |
| [Delete A Token For A Service Account.](actions/deleteserviceaccounttoken.md) | `DELETE /api/admin/service-account/{id}/token/{tokenId}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Delete A Signal Endpoint.](actions/deletesignalendpoint.md) | `DELETE /api/admin/signal-endpoints/{id}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Delete A Signal Endpoint Token.](actions/deletesignalendpointtoken.md) | `DELETE /api/admin/signal-endpoints/{signalEndpointId}/tokens/{id}` | [docs](https://docs.getunleash.io/api) |
| [Delete A Tag.](actions/deletetag.md) | `DELETE /api/admin/tags/{type}/{value}` | [docs](https://docs.getunleash.io/api) |
| [Delete A Tag Type](actions/deletetagtype.md) | `DELETE /api/admin/tag-types/{name}` | [docs](https://docs.getunleash.io/api) |
| [Delete A User](actions/deleteuser.md) | `DELETE /api/admin/user-admin/{id}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Disables An Action Set.](actions/disableactions.md) | `POST /api/admin/projects/{projectId}/actions/{id}/off` | [docs](https://docs.getunleash.io/api) |
| [Disables A Banner.](actions/disablebanner.md) | `POST /api/admin/banners/{id}/off` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Disables A Signal Endpoint.](actions/disablesignalendpoint.md) | `POST /api/admin/signal-endpoints/{id}/off` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Disconnect All Clients.](actions/disconnectall.md) | `POST /api/admin/streaming/disconnect-all` | [docs](https://docs.getunleash.io/api) |
| [Get Or Create Valid Tokens For The Requested Environment](actions/edgecreateorreturntokens.md) | `POST /edge/issue-token` | [docs](https://docs.getunleash.io/api) |
| [Heartbeat For Enterprise Edge Instances.](actions/edgeinstanceheartbeat.md) | `POST /api/client/edge-licensing/heartbeat` | [docs](https://docs.getunleash.io/api) |
| [Edits A Single Change In A Change Request](actions/editchange.md) | `PUT /api/admin/projects/{projectId}/change-requests/{changeRequestId}/changes/{changeId}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Enables An Action Set.](actions/enableactions.md) | `POST /api/admin/projects/{projectId}/actions/{id}/on` | [docs](https://docs.getunleash.io/api) |
| [Enables A Banner.](actions/enablebanner.md) | `POST /api/admin/banners/{id}/on` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Enables A Signal Endpoint.](actions/enablesignalendpoint.md) | `POST /api/admin/signal-endpoints/{id}/on` | [docs](https://docs.getunleash.io/api) |
| [Generates A New Scim Api Token.](actions/generatenewtoken.md) | `POST /api/admin/scim-settings/generate-new-token` | [docs](https://docs.getunleash.io/api) |
| [Get Strategies That Use A Context Field](actions/get-api-admin-context-contextfield-strategies.md) | `GET /api/admin/context/{contextField}/strategies` | [docs](https://docs.getunleash.io/api) |
| [Get All Feature Types](actions/get-api-admin-feature-types.md) | `GET /api/admin/feature-types` | [docs](https://docs.getunleash.io/api) |
| [Get All Tags For A Feature.](actions/get-api-admin-features-featurename-tags.md) | `GET /api/admin/features/{featureName}/tags` | [docs](https://docs.getunleash.io/api) |
| [Search And Filter Features](actions/get-api-admin-search-features.md) | `GET /api/admin/search/features` | [docs](https://docs.getunleash.io/api) |
| [Get Strategies That Reference Segment](actions/get-api-admin-segments-id-strategies.md) | `GET /api/admin/segments/{id}/strategies` | [docs](https://docs.getunleash.io/api) |
| [Get Strategy Segments](actions/get-api-admin-segments-strategies-strategyid.md) | `GET /api/admin/segments/strategies/{strategyId}` | [docs](https://docs.getunleash.io/api) |
| [Get All Strategies](actions/get-api-admin-strategies.md) | `GET /api/admin/strategies` | [docs](https://docs.getunleash.io/api) |
| [Get A Strategy Definition](actions/get-api-admin-strategies-name.md) | `GET /api/admin/strategies/{name}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Partial Updates (Sdk)](actions/get-api-client-delta.md) | `GET /api/client/delta` | [docs](https://docs.getunleash.io/api) |
| [Get All Flags (Sdk)](actions/get-api-client-features.md) | `GET /api/client/features` | [docs](https://docs.getunleash.io/api) |
| [Get A Single Feature Flag](actions/get-api-client-features-featurename.md) | `GET /api/client/features/{featureName}` | [docs](https://docs.getunleash.io/api) |
| [Get projects](actions/get-projects.md) | `GET /api/admin/projects` | [docs](https://docs.getunleash.io/api) |
| [Gets Access Overview](actions/getaccessoverview.md) | `GET /api/admin/access/overview` | [docs](https://docs.getunleash.io/api) |
| [Get The Number Of Change Requests You Can Do Something With](actions/getactionablechangerequests.md) | `GET /api/admin/projects/{projectId}/change-requests/actionable` | [docs](https://docs.getunleash.io/api) |
| [[Beta] List Action Sets.](actions/getactions.md) | `GET /api/admin/projects/{projectId}/actions` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Configuration For The Actions Ui.](actions/getactionsconfig.md) | `GET /api/admin/projects/{projectId}/actions/config` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Action Events For A Specific Action Set.](actions/getactionsevents.md) | `GET /api/admin/projects/{projectId}/actions/{id}/events` | [docs](https://docs.getunleash.io/api) |
| [Get A Specific Addon](actions/getaddon.md) | `GET /api/admin/addons/{id}` | [docs](https://docs.getunleash.io/api) |
| [Get All Addons And Providers](actions/getaddons.md) | `GET /api/admin/addons` | [docs](https://docs.getunleash.io/api) |
| [Get Total Count Of Admin Accounts](actions/getadmincount.md) | `GET /api/admin/user-admin/admin-count` | [docs](https://docs.getunleash.io/api) |
| [Batch Evaluate An Unleash Context Against A Set Of Environments And Projects.](actions/getadvancedplayground.md) | `POST /api/admin/playground/advanced` | [docs](https://docs.getunleash.io/api) |
| [Get Api Tokens](actions/getallapitokens.md) | `GET /api/admin/api-tokens` | [docs](https://docs.getunleash.io/api) |
| [Get All Environments](actions/getallenvironments.md) | `GET /api/admin/environments` | [docs](https://docs.getunleash.io/api) |
| [Retrieves All Licensed Users Data.](actions/getalllicensedusers.md) | `GET /api/admin/licensed-users` | [docs](https://docs.getunleash.io/api) |
| [Get Public Signup Tokens](actions/getallpublicsignuptokens.md) | `GET /api/admin/invite-link/tokens` | [docs](https://docs.getunleash.io/api) |
| [Get Api Tokens By Name](actions/getapitokensbyname.md) | `GET /api/admin/api-tokens/{name}` | [docs](https://docs.getunleash.io/api) |
| [Get Application Data](actions/getapplication.md) | `GET /api/admin/metrics/applications/{appName}` | [docs](https://docs.getunleash.io/api) |
| [Get Application Environment Instances (Last 24H)](actions/getapplicationenvironmentinstances.md) | `GET /api/admin/metrics/instances/{appName}/environment/{environment}` | [docs](https://docs.getunleash.io/api) |
| [Get Application Overview](actions/getapplicationoverview.md) | `GET /api/admin/metrics/applications/{appName}/overview` | [docs](https://docs.getunleash.io/api) |
| [Get All Applications](actions/getapplications.md) | `GET /api/admin/metrics/applications` | [docs](https://docs.getunleash.io/api) |
| [This Endpoint Will Return Users Available To Review/Approve This Change Request](actions/getavailablechangerequestreviewers.md) | `GET /api/admin/projects/{projectId}/change-requests/available-reviewers/{environment}` | [docs](https://docs.getunleash.io/api) |
| [Get All Banners.](actions/getbanners.md) | `GET /api/admin/banners` | [docs](https://docs.getunleash.io/api) |
| [Get Basic User And Group Information](actions/getbaseusersandgroups.md) | `GET /api/admin/user-admin/access` | [docs](https://docs.getunleash.io/api) |
| [Retrieves One Change Request By Id](actions/getchangerequest.md) | `GET /api/admin/projects/{projectId}/change-requests/{id}` | [docs](https://docs.getunleash.io/api) |
| [This Endpoint Fetches The Requested Approvers Of A Change Request](actions/getchangerequestapprovers.md) | `GET /api/admin/projects/{projectId}/change-requests/{id}/approvers` | [docs](https://docs.getunleash.io/api) |
| [Evaluate An Unleash Context Against A Change Request Preview.](actions/getchangerequestplayground.md) | `POST /api/admin/playground/change-request/{id}` | [docs](https://docs.getunleash.io/api) |
| [Retrieves Number Of Project Change Requests In Each State](actions/getchangerequestscount.md) | `GET /api/admin/projects/{projectId}/change-requests/count` | [docs](https://docs.getunleash.io/api) |
| [Retrieves All Change Requests For A Project](actions/getchangerequestsforproject.md) | `GET /api/admin/projects/{projectId}/change-requests` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Aggregated Metered Connections For A Given Time Period.](actions/getconnectionsforperiod.md) | `GET /api/admin/metrics/connection` | [docs](https://docs.getunleash.io/api) |
| [Gets Context Field](actions/getcontextfield.md) | `GET /api/admin/context/{contextField}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Gets Context Field](actions/getcontextfieldforproject.md) | `GET /api/admin/projects/{projectId}/context/{contextField}` | [docs](https://docs.getunleash.io/api) |
| [Gets Configured Context Fields](actions/getcontextfields.md) | `GET /api/admin/context` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Gets Configured Context Fields](actions/getcontextfieldsforproject.md) | `GET /api/admin/projects/{projectId}/context` | [docs](https://docs.getunleash.io/api) |
| [Get Stored Custom Metrics](actions/getcustommetrics.md) | `GET /api/admin/custom-metrics` | [docs](https://docs.getunleash.io/api) |
| [Get Detailed Invoices](actions/getdetailedinvoices.md) | `GET /api/admin/invoices/list` | [docs](https://docs.getunleash.io/api) |
| [Get The Environment With `Name`](actions/getenvironment.md) | `GET /api/admin/environments/{name}` | [docs](https://docs.getunleash.io/api) |
| [Get Variants For A Feature In An Environment](actions/getenvironmentfeaturevariants.md) | `GET /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/variants` | [docs](https://docs.getunleash.io/api) |
| [Get A List Of All Users That Have Created Events](actions/geteventcreators.md) | `GET /api/admin/event-creators` | [docs](https://docs.getunleash.io/api) |
| [Get The Most Recent Events From The Unleash Instance Or All Events Related To A](actions/getevents.md) | `GET /api/admin/events` | [docs](https://docs.getunleash.io/api) |
| [Get All Events Related To A Specific Feature Flag.](actions/geteventsfortoggle.md) | `GET /api/admin/events/{featureName}` | [docs](https://docs.getunleash.io/api) |
| [Get A Feature](actions/getfeature.md) | `GET /api/admin/projects/{projectId}/features/{featureName}` | [docs](https://docs.getunleash.io/api) |
| [Get A Feature Environment](actions/getfeatureenvironment.md) | `GET /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Feature Lifecycle](actions/getfeaturelifecycle.md) | `GET /api/admin/projects/{projectId}/features/{featureName}/lifecycle` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get All Features Lifecycle Stage Count](actions/getfeaturelifecyclestagecount.md) | `GET /api/admin/lifecycle/count` | [docs](https://docs.getunleash.io/api) |
| [Get All Features In A Project](actions/getfeatures.md) | `GET /api/admin/projects/{projectId}/features` | [docs](https://docs.getunleash.io/api) |
| [Get Feature Flag Strategies](actions/getfeaturestrategies.md) | `GET /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies` | [docs](https://docs.getunleash.io/api) |
| [Get A Strategy Configuration](actions/getfeaturestrategy.md) | `GET /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies/{strategyId}` | [docs](https://docs.getunleash.io/api) |
| [Last Hour Of Usage And A List Of Applications That Have Reported Seeing This Fea](actions/getfeatureusagesummary.md) | `GET /api/admin/client-metrics/features/{name}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Impact Metrics Configurations For A Single Feature](actions/getflagimpactmetricsconfigsbyfeature.md) | `GET /api/admin/projects/{projectId}/features/{featureName}/impact-metrics/config` | [docs](https://docs.getunleash.io/api) |
| [Retrieve Enabled Feature Flags For The Provided Context, Using Post.](actions/getfrontendapifeatureswithpost.md) | `POST /api/frontend` | [docs](https://docs.getunleash.io/api) |
| [Retrieve Enabled Feature Flags For The Provided Context.](actions/getfrontendfeatures.md) | `GET /api/frontend` | [docs](https://docs.getunleash.io/api) |
| [Get A Single Group](actions/getgroup.md) | `GET /api/admin/groups/{groupId}` | [docs](https://docs.getunleash.io/api) |
| [Get A List Of Groups](actions/getgroups.md) | `GET /api/admin/groups` | [docs](https://docs.getunleash.io/api) |
| [Get Instance Operational Status](actions/gethealth.md) | `GET /health` | [docs](https://docs.getunleash.io/api) |
| [Gets Inactive Users](actions/getinactiveusers.md) | `GET /api/admin/user-admin/inactive` | [docs](https://docs.getunleash.io/api) |
| [Instance Usage Statistics](actions/getinstanceadminstats.md) | `GET /api/admin/instance-admin/statistics` | [docs](https://docs.getunleash.io/api) |
| [Instance Usage Statistics](actions/getinstanceadminstatscsv.md) | `GET /api/admin/instance-admin/statistics/csv` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Impact Metrics Configuration For The Instance](actions/getinstanceimpactmetricsconfigs.md) | `GET /api/admin/impact-metrics/config` | [docs](https://docs.getunleash.io/api) |
| [Get Instance Information](actions/getinstanceinsights.md) | `GET /api/admin/insights` | [docs](https://docs.getunleash.io/api) |
| [Get Integration Events For A Specific Integration Configuration.](actions/getintegrationevents.md) | `GET /api/admin/addons/{id}/events` | [docs](https://docs.getunleash.io/api) |
| [Get Invoices](actions/getinvoices.md) | `GET /api/admin/invoices` | [docs](https://docs.getunleash.io/api) |
| [Get Lifecycle Trends](actions/getlifecycletrends.md) | `GET /api/admin/insights/lifecycle` | [docs](https://docs.getunleash.io/api) |
| [Get All Login Events.](actions/getloginhistory.md) | `GET /api/admin/logins` | [docs](https://docs.getunleash.io/api) |
| [Get Maintenance Mode Status](actions/getmaintenance.md) | `GET /api/admin/maintenance` | [docs](https://docs.getunleash.io/api) |
| [Get Your Own User Details](actions/getme.md) | `GET /api/admin/user` | [docs](https://docs.getunleash.io/api) |
| [Retrieves A List Of Notifications](actions/getnotifications.md) | `GET /api/admin/notifications` | [docs](https://docs.getunleash.io/api) |
| [Get Oidc Auth Settings](actions/getoidcsettings.md) | `GET /api/admin/auth/oidc/settings` | [docs](https://docs.getunleash.io/api) |
| [Retrieves Pending Change Requests In Configured Environments](actions/getopenchangerequestsforuser.md) | `GET /api/admin/projects/{projectId}/change-requests/open` | [docs](https://docs.getunleash.io/api) |
| [Get Outdated Project Sdks](actions/getoutdatedprojectsdks.md) | `GET /api/admin/projects/{projectId}/sdks/outdated` | [docs](https://docs.getunleash.io/api) |
| [Get Outdated Sdks](actions/getoutdatedsdks.md) | `GET /api/admin/metrics/sdks/outdated` | [docs](https://docs.getunleash.io/api) |
| [Get All Personal Access Tokens (Pats) For The Current User.](actions/getpats.md) | `GET /api/admin/user/tokens` | [docs](https://docs.getunleash.io/api) |
| [Retrieves All Pending Change Requests Referencing A Feature In The Project](actions/getpendingchangerequestsforfeature.md) | `GET /api/admin/projects/{projectId}/change-requests/pending/{featureName}` | [docs](https://docs.getunleash.io/api) |
| [Retrieves Pending Change Requests In Configured Environments](actions/getpendingchangerequestsforuser.md) | `GET /api/admin/projects/{projectId}/change-requests/pending` | [docs](https://docs.getunleash.io/api) |
| [Gets Available Permissions](actions/getpermissions.md) | `GET /api/admin/permissions` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Personal Dashboard](actions/getpersonaldashboard.md) | `GET /api/admin/personal-dashboard` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Personal Project Details](actions/getpersonaldashboardprojectdetails.md) | `GET /api/admin/personal-dashboard/{projectId}` | [docs](https://docs.getunleash.io/api) |
| [Evaluate An Unleash Context Against A Set Of Environments And Projects.](actions/getplayground.md) | `POST /api/admin/playground` | [docs](https://docs.getunleash.io/api) |
| [Get Your Own User Profile](actions/getprofile.md) | `GET /api/admin/user/profile` | [docs](https://docs.getunleash.io/api) |
| [Get Users And Groups In Project](actions/getprojectaccess.md) | `GET /api/admin/projects/{projectId}/access` | [docs](https://docs.getunleash.io/api) |
| [Get Api Tokens For Project.](actions/getprojectapitokens.md) | `GET /api/admin/projects/{projectId}/api-tokens` | [docs](https://docs.getunleash.io/api) |
| [Get A List Of All Applications For A Project.](actions/getprojectapplications.md) | `GET /api/admin/projects/{projectId}/applications` | [docs](https://docs.getunleash.io/api) |
| [Retrieves Change Request Configuration For A Project](actions/getprojectchangerequestconfig.md) | `GET /api/admin/projects/{projectId}/change-requests/config` | [docs](https://docs.getunleash.io/api) |
| [Get An Overview Project Dora Metrics.](actions/getprojectdora.md) | `GET /api/admin/projects/{projectId}/dora` | [docs](https://docs.getunleash.io/api) |
| [Get The Environments Available To A Project](actions/getprojectenvironments.md) | `GET /api/admin/environments/project/{projectId}` | [docs](https://docs.getunleash.io/api) |
| [Get A List Of All Flag Creators For A Project.](actions/getprojectflagcreators.md) | `GET /api/admin/projects/{projectId}/flag-creators` | [docs](https://docs.getunleash.io/api) |
| [Get A Health Report For A Project.](actions/getprojecthealthreport.md) | `GET /api/admin/projects/{projectId}/health-report` | [docs](https://docs.getunleash.io/api) |
| [Get An Overview Of A Project Insights.](actions/getprojectinsights.md) | `GET /api/admin/projects/{projectId}/insights` | [docs](https://docs.getunleash.io/api) |
| [Get An Overview Of A Project.](actions/getprojectoverview.md) | `GET /api/admin/projects/{projectId}/overview` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Project Status](actions/getprojectstatus.md) | `GET /api/admin/projects/{projectId}/status` | [docs](https://docs.getunleash.io/api) |
| [Get Metrics In Prometheus Format](actions/getprometheusmetrics.md) | `GET /api/admin/custom-metrics/prometheus` | [docs](https://docs.getunleash.io/api) |
| [Retrieve A Token](actions/getpublicsignuptoken.md) | `GET /api/admin/invite-link/tokens/{token}` | [docs](https://docs.getunleash.io/api) |
| [Get Feature Metrics](actions/getrawfeaturemetrics.md) | `GET /api/admin/client-metrics/features/{name}/raw` | [docs](https://docs.getunleash.io/api) |
| [Get Instance Readiness Status](actions/getready.md) | `GET /ready` | [docs](https://docs.getunleash.io/api) |
| [Get Release Plans.](actions/getreleaseplans.md) | `GET /api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans` | [docs](https://docs.getunleash.io/api) |
| [Get A Release Template By Its Id.](actions/getreleasetemplate.md) | `GET /api/admin/release-plan-templates/{templateId}` | [docs](https://docs.getunleash.io/api) |
| [Get All Release Templates.](actions/getreleasetemplates.md) | `GET /api/admin/release-plan-templates` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Aggregated Metered Requests For A Given Time Period.](actions/getrequestsforperiod.md) | `GET /api/admin/metrics/request` | [docs](https://docs.getunleash.io/api) |
| [Gets Usage Data](actions/getrequestspersecond.md) | `GET /api/admin/metrics/rps` | [docs](https://docs.getunleash.io/api) |
| [Get A Single Role](actions/getrolebyid.md) | `GET /api/admin/roles/{roleId}` | [docs](https://docs.getunleash.io/api) |
| [Get Project Role Mappings](actions/getroleprojectaccess.md) | `GET /api/admin/projects/roles/{roleId}/access` | [docs](https://docs.getunleash.io/api) |
| [Get A List Of Roles](actions/getroles.md) | `GET /api/admin/roles` | [docs](https://docs.getunleash.io/api) |
| [Get Saml Auth Settings](actions/getsamlsettings.md) | `GET /api/admin/auth/saml/settings` | [docs](https://docs.getunleash.io/api) |
| [Get Scheduled Change Requests Matching A Query.](actions/getscheduledchangerequests.md) | `GET /api/admin/projects/{projectId}/change-requests/scheduled` | [docs](https://docs.getunleash.io/api) |
| [Get Scim Settings.](actions/getscimsettings.md) | `GET /api/admin/scim-settings` | [docs](https://docs.getunleash.io/api) |
| [Get A Segment](actions/getsegment.md) | `GET /api/admin/segments/{id}` | [docs](https://docs.getunleash.io/api) |
| [Get All Segments](actions/getsegments.md) | `GET /api/admin/segments` | [docs](https://docs.getunleash.io/api) |
| [Returns The List Of Permissions For The Service Account.](actions/getserviceaccountpermissions.md) | `GET /api/admin/service-account/{id}/permissions` | [docs](https://docs.getunleash.io/api) |
| [List Service Accounts.](actions/getserviceaccounts.md) | `GET /api/admin/service-account` | [docs](https://docs.getunleash.io/api) |
| [List All Tokens For A Service Account.](actions/getserviceaccounttokens.md) | `GET /api/admin/service-account/{id}/token` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get All Signal Endpoints.](actions/getsignalendpoints.md) | `GET /api/admin/signal-endpoints` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Signals Originated From A Specific Signal Endpoint.](actions/getsignalendpointsignals.md) | `GET /api/admin/signal-endpoints/{signalEndpointId}/signals` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get All Signal Endpoint Tokens For A Specific Signal Endpoint.](actions/getsignalendpointtokens.md) | `GET /api/admin/signal-endpoints/{signalEndpointId}/tokens` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get All Signals That Match The Query Parameter Criteria.](actions/getsignals.md) | `GET /api/admin/signals` | [docs](https://docs.getunleash.io/api) |
| [Get Signup Data](actions/getsignupdata.md) | `GET /api/admin/signup` | [docs](https://docs.getunleash.io/api) |
| [Get Simple Auth Settings](actions/getsimplesettings.md) | `GET /api/admin/auth/simple/settings` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Get Strategies That Use A Context Field](actions/getstrategiesbycontextfieldforproject.md) | `GET /api/admin/projects/{projectId}/context/{contextField}/strategies` | [docs](https://docs.getunleash.io/api) |
| [Get A Tag By Type And Value.](actions/gettag.md) | `GET /api/admin/tags/{type}/{value}` | [docs](https://docs.getunleash.io/api) |
| [List All Tags.](actions/gettags.md) | `GET /api/admin/tags` | [docs](https://docs.getunleash.io/api) |
| [List All Tags Of A Given Type.](actions/gettagsbytype.md) | `GET /api/admin/tags/{type}` | [docs](https://docs.getunleash.io/api) |
| [Get A Tag Type](actions/gettagtype.md) | `GET /api/admin/tag-types/{name}` | [docs](https://docs.getunleash.io/api) |
| [Get All Tag Types](actions/gettagtypes.md) | `GET /api/admin/tag-types` | [docs](https://docs.getunleash.io/api) |
| [Get Telemetry Settings](actions/gettelemetrysettings.md) | `GET /api/admin/telemetry/settings` | [docs](https://docs.getunleash.io/api) |
| [Get Aggregated Traffic Data For A Given Time Period.](actions/gettrafficdatausageforperiod.md) | `GET /api/admin/metrics/traffic` | [docs](https://docs.getunleash.io/api) |
| [Get Ui Configuration](actions/getuiconfig.md) | `GET /api/admin/ui-config` | [docs](https://docs.getunleash.io/api) |
| [Get Unknown Flags](actions/getunknownflags.md) | `GET /api/admin/metrics/unknown-flags` | [docs](https://docs.getunleash.io/api) |
| [Get User](actions/getuser.md) | `GET /api/admin/user-admin/{id}` | [docs](https://docs.getunleash.io/api) |
| [Get All Pending User Access Requests.](actions/getuseraccessrequests.md) | `GET /api/admin/user-access-requests` | [docs](https://docs.getunleash.io/api) |
| [Get Roles For Currently Logged In User](actions/getuserroles.md) | `GET /api/admin/user/roles` | [docs](https://docs.getunleash.io/api) |
| [Get All Users And [Root Roles](Https://Docs.Getunleash.Io/Concepts/Rbac#Predefin](actions/getusers.md) | `GET /api/admin/user-admin` | [docs](https://docs.getunleash.io/api) |
| [Check Which Tokens Are Valid](actions/getvalidtokens.md) | `POST /edge/validate` | [docs](https://docs.getunleash.io/api) |
| [List Parent Options.](actions/listparentoptions.md) | `GET /api/admin/projects/{projectId}/features/{child}/parents` | [docs](https://docs.getunleash.io/api) |
| [List Parent Feature Variants.](actions/listparentvariantoptions.md) | `GET /api/admin/projects/{projectId}/features/{parent}/parent-variants` | [docs](https://docs.getunleash.io/api) |
| [Log In](actions/login.md) | `POST /auth/simple/login` | [docs](https://docs.getunleash.io/api) |
| [Mark Notifications As Read](actions/marknotificationsasread.md) | `POST /api/admin/notifications/read` | [docs](https://docs.getunleash.io/api) |
| [Add A Release Plan.](actions/oldaddreleaseplan.md) | `POST /api/admin/projects/{project}/features/{featureName}/environments/{environment}/release_plans` | [docs](https://docs.getunleash.io/api) |
| [Get Release Plans.](actions/oldgetreleaseplans.md) | `GET /api/admin/projects/{project}/features/{featureName}/environments/{environment}/release_plans` | [docs](https://docs.getunleash.io/api) |
| [Remove A Release Plan.](actions/oldremovereleaseplan.md) | `DELETE /api/admin/projects/{project}/features/{featureName}/environments/{environment}/release_plans/{planId}` | [docs](https://docs.getunleash.io/api) |
| [Start A Release Plan Milestone.](actions/oldstartmilestone.md) | `POST /api/admin/projects/{project}/features/{featureName}/environments/{environment}/release_plans/{planId}/milestones/{milestoneId}/start` | [docs](https://docs.getunleash.io/api) |
| [Create (Overwrite) Variants For A Feature In An Environment](actions/overwriteenvironmentfeaturevariants.md) | `PUT /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/variants` | [docs](https://docs.getunleash.io/api) |
| [Create (Overwrite) Variants For A Feature Flag In Multiple Environments](actions/overwritefeaturevariantsonenvironments.md) | `PUT /api/admin/projects/{projectId}/features/{featureName}/variants-batch` | [docs](https://docs.getunleash.io/api) |
| [Patch A Feature's Variants In An Environment](actions/patchenvironmentsfeaturevariants.md) | `PATCH /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/variants` | [docs](https://docs.getunleash.io/api) |
| [Modify A Feature Flag](actions/patchfeature.md) | `PATCH /api/admin/projects/{projectId}/features/{featureName}` | [docs](https://docs.getunleash.io/api) |
| [Change Specific Properties Of A Strategy](actions/patchfeaturestrategy.md) | `PATCH /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies/{strategyId}` | [docs](https://docs.getunleash.io/api) |
| [Export Feature Flags From An Environment](actions/post-api-admin-features-batch-export.md) | `POST /api/admin/features-batch/export` | [docs](https://docs.getunleash.io/api) |
| [Import Feature Flags](actions/post-api-admin-features-batch-import.md) | `POST /api/admin/features-batch/import` | [docs](https://docs.getunleash.io/api) |
| [Validate Feature Import Data](actions/post-api-admin-features-batch-validate.md) | `POST /api/admin/features-batch/validate` | [docs](https://docs.getunleash.io/api) |
| [Adds A Tag To A Feature.](actions/post-api-admin-features-featurename-tags.md) | `POST /api/admin/features/{featureName}/tags` | [docs](https://docs.getunleash.io/api) |
| [Validate A Feature Flag Name.](actions/post-api-admin-features-validate.md) | `POST /api/admin/features/validate` | [docs](https://docs.getunleash.io/api) |
| [Adds A Strategy To A Milestone.](actions/post-api-admin-release-plan-templates-templateid-milestones-milestoneid-strategies.md) | `POST /api/admin/release-plan-templates/{templateId}/milestones/{milestoneId}/strategies` | [docs](https://docs.getunleash.io/api) |
| [Update Strategy Segments](actions/post-api-admin-segments-strategies.md) | `POST /api/admin/segments/strategies` | [docs](https://docs.getunleash.io/api) |
| [Create A Strategy](actions/post-api-admin-strategies.md) | `POST /api/admin/strategies` | [docs](https://docs.getunleash.io/api) |
| [Deprecate A Strategy](actions/post-api-admin-strategies-strategyname-deprecate.md) | `POST /api/admin/strategies/{strategyName}/deprecate` | [docs](https://docs.getunleash.io/api) |
| [Reactivate A Strategy](actions/post-api-admin-strategies-strategyname-reactivate.md) | `POST /api/admin/strategies/{strategyName}/reactivate` | [docs](https://docs.getunleash.io/api) |
| [Update Feature Type Lifetime](actions/put-api-admin-feature-types-id-lifetime.md) | `PUT /api/admin/feature-types/{id}/lifetime` | [docs](https://docs.getunleash.io/api) |
| [Updates Multiple Tags For A Feature.](actions/put-api-admin-features-featurename-tags.md) | `PUT /api/admin/features/{featureName}/tags` | [docs](https://docs.getunleash.io/api) |
| [Updates A Strategy Attached To A Milestone](actions/put-api-admin-release-plan-templates-templateid-milestones-milestoneid-strategies-strategy.md) | `PUT /api/admin/release-plan-templates/{templateId}/milestones/{milestoneId}/strategies/{strategyId}` | [docs](https://docs.getunleash.io/api) |
| [Update A Strategy Type](actions/put-api-admin-strategies-name.md) | `PUT /api/admin/strategies/{name}` | [docs](https://docs.getunleash.io/api) |
| [Reads The Unleash License.](actions/readlicense.md) | `GET /api/admin/license` | [docs](https://docs.getunleash.io/api) |
| [Register A Client Sdk](actions/registerclientapplication.md) | `POST /api/client/register` | [docs](https://docs.getunleash.io/api) |
| [Register Client Usage Metrics](actions/registerclientmetrics.md) | `POST /api/client/metrics` | [docs](https://docs.getunleash.io/api) |
| [Register Edge Observability Metrics.](actions/registeredgeobservabilitymetrics.md) | `POST /api/client/metrics/edge` | [docs](https://docs.getunleash.io/api) |
| [Register A Client Sdk](actions/registerfrontendclient.md) | `POST /api/frontend/client/register` | [docs](https://docs.getunleash.io/api) |
| [Register Client Usage Metrics](actions/registerfrontendmetrics.md) | `POST /api/frontend/client/metrics` | [docs](https://docs.getunleash.io/api) |
| [Reject A User Access Request.](actions/rejectuseraccessrequest.md) | `DELETE /api/admin/user-access-requests/{id}` | [docs](https://docs.getunleash.io/api) |
| [Deletes An Environment By Name](actions/removeenvironment.md) | `DELETE /api/admin/environments/{name}` | [docs](https://docs.getunleash.io/api) |
| [Remove An Environment From A Project.](actions/removeenvironmentfromproject.md) | `DELETE /api/admin/projects/{projectId}/environments/{environment}` | [docs](https://docs.getunleash.io/api) |
| [Remove Feature From Favorites](actions/removefavoritefeature.md) | `DELETE /api/admin/projects/{projectId}/features/{featureName}/favorites` | [docs](https://docs.getunleash.io/api) |
| [Remove Project From Favorites](actions/removefavoriteproject.md) | `DELETE /api/admin/projects/{projectId}/favorites` | [docs](https://docs.getunleash.io/api) |
| [Remove Project Access For A Group](actions/removegroupaccess.md) | `DELETE /api/admin/projects/{projectId}/groups/{groupId}/roles` | [docs](https://docs.getunleash.io/api) |
| [Remove A Release Plan.](actions/removereleaseplan.md) | `DELETE /api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans/{planId}` | [docs](https://docs.getunleash.io/api) |
| [Removes An Existing Milestone](actions/removereleasetemplatemilestone.md) | `DELETE /api/admin/release-plan-templates/{templateId}/milestones/{milestoneId}` | [docs](https://docs.getunleash.io/api) |
| [Deletes A Segment By Id](actions/removesegment.md) | `DELETE /api/admin/segments/{id}` | [docs](https://docs.getunleash.io/api) |
| [Remove Project Access For A User](actions/removeuseraccess.md) | `DELETE /api/admin/projects/{projectId}/users/{userId}/roles` | [docs](https://docs.getunleash.io/api) |
| [Reset User Password](actions/resetuserpassword.md) | `POST /api/admin/user-admin/reset-password` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Resume Paused Milestone Progressions](actions/resumemilestoneprogressions.md) | `POST /api/admin/projects/{project}/features/{featureName}/environments/{environment}/progressions/{planId}/resume` | [docs](https://docs.getunleash.io/api) |
| [Revives A Feature](actions/revivefeature.md) | `POST /api/admin/archive/revive/{featureName}` | [docs](https://docs.getunleash.io/api) |
| [Revives A List Of Features](actions/revivefeatures.md) | `POST /api/admin/projects/{projectId}/revive` | [docs](https://docs.getunleash.io/api) |
| [Revive Project](actions/reviveproject.md) | `POST /api/admin/projects/revive/{projectId}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Save Flag Level Impact Metrics Configuration](actions/savefeatureimpactmetricsconfig.md) | `POST /api/admin/projects/{projectId}/features/{featureName}/impact-metrics/config` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Save Instance Level Impact Metrics Configuration](actions/saveinstanceimpactmetricsconfig.md) | `POST /api/admin/impact-metrics/config` | [docs](https://docs.getunleash.io/api) |
| [Search change requests](actions/search-change-requests.md) | `GET /api/admin/search/change-requests` | [docs](https://docs.getunleash.io/api) |
| [Search For Events](actions/searchevents.md) | `GET /api/admin/search/events` | [docs](https://docs.getunleash.io/api) |
| [Search Users](actions/searchusers.md) | `GET /api/admin/user-admin/search` | [docs](https://docs.getunleash.io/api) |
| [Reset Password](actions/sendresetpasswordemail.md) | `POST /auth/reset/password-email` | [docs](https://docs.getunleash.io/api) |
| [Sets Allowed Cors Origins](actions/setcors.md) | `POST /api/admin/ui-config/cors` | [docs](https://docs.getunleash.io/api) |
| [Set Oidc Settings](actions/setoidcsettings.md) | `POST /api/admin/auth/oidc/settings` | [docs](https://docs.getunleash.io/api) |
| [Set Users And Groups To Roles In The Current Project](actions/setprojectaccess.md) | `PUT /api/admin/projects/{projectId}/access` | [docs](https://docs.getunleash.io/api) |
| [Sets Roles For Group](actions/setrolesforgroup.md) | `PUT /api/admin/projects/{projectId}/groups/{groupId}/roles` | [docs](https://docs.getunleash.io/api) |
| [Sets Roles For User](actions/setrolesforuser.md) | `PUT /api/admin/projects/{projectId}/users/{userId}/roles` | [docs](https://docs.getunleash.io/api) |
| [Update Saml Auth Settings](actions/setsamlsettings.md) | `POST /api/admin/auth/saml/settings` | [docs](https://docs.getunleash.io/api) |
| [Set Scim Settings.](actions/setscimsettings.md) | `POST /api/admin/scim-settings` | [docs](https://docs.getunleash.io/api) |
| [Update Simple Auth Settings](actions/setsimplesettings.md) | `POST /api/admin/auth/simple/settings` | [docs](https://docs.getunleash.io/api) |
| [Set Strategy Sort Order](actions/setstrategysortorder.md) | `POST /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies/set-sort-order` | [docs](https://docs.getunleash.io/api) |
| [Mark Features As Stale / Not Stale](actions/stalefeatures.md) | `POST /api/admin/projects/{projectId}/stale` | [docs](https://docs.getunleash.io/api) |
| [Start A Release Plan Milestone.](actions/startmilestone.md) | `POST /api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans/{planId}/milestones/{milestoneId}/start` | [docs](https://docs.getunleash.io/api) |
| [Submit Signup Data.](actions/submitsignupdata.md) | `POST /api/admin/signup` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Subscribe To Email Subscription](actions/subscribeemailsubscription.md) | `PUT /api/admin/email-subscription/{subscription}` | [docs](https://docs.getunleash.io/api) |
| [Toggle The Environment With `Name` Off](actions/toggleenvironmentoff.md) | `POST /api/admin/environments/{name}/off` | [docs](https://docs.getunleash.io/api) |
| [Toggle The Environment With `Name` On](actions/toggleenvironmenton.md) | `POST /api/admin/environments/{name}/on` | [docs](https://docs.getunleash.io/api) |
| [Disable A Feature Flag](actions/togglefeatureenvironmentoff.md) | `POST /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/off` | [docs](https://docs.getunleash.io/api) |
| [Enable A Feature Flag](actions/togglefeatureenvironmenton.md) | `POST /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/on` | [docs](https://docs.getunleash.io/api) |
| [Enabled/Disabled Maintenance Mode](actions/togglemaintenance.md) | `POST /api/admin/maintenance` | [docs](https://docs.getunleash.io/api) |
| [Accepts Errors From The Ui Client](actions/uiobservability.md) | `POST /api/admin/record-ui-error` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Set Feature Uncompleted](actions/uncomplete.md) | `POST /api/admin/projects/{projectId}/features/{featureName}/lifecycle/uncomplete` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Unsubscribe From Email Subscription](actions/unsubscribeemailsubscription.md) | `DELETE /api/admin/email-subscription/{subscription}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Update An Action Set.](actions/updateactions.md) | `PUT /api/admin/projects/{projectId}/actions/{id}` | [docs](https://docs.getunleash.io/api) |
| [Update An Addon](actions/updateaddon.md) | `PUT /api/admin/addons/{id}` | [docs](https://docs.getunleash.io/api) |
| [Update Api Token](actions/updateapitoken.md) | `PUT /api/admin/api-tokens/{token}` | [docs](https://docs.getunleash.io/api) |
| [Update A Banner.](actions/updatebanner.md) | `PUT /api/admin/banners/{id}` | [docs](https://docs.getunleash.io/api) |
| [This Endpoint Will Update The State Of A Change Request](actions/updatechangerequeststate.md) | `PUT /api/admin/projects/{projectId}/change-requests/{id}/state` | [docs](https://docs.getunleash.io/api) |
| [This Endpoint Will Update The Custom Title Of A Change Request](actions/updatechangerequesttitle.md) | `PUT /api/admin/projects/{projectId}/change-requests/{id}/title` | [docs](https://docs.getunleash.io/api) |
| [Update An Existing Context Field](actions/updatecontextfield.md) | `PUT /api/admin/context/{contextField}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Update An Existing Context Field](actions/updatecontextfieldforproject.md) | `PUT /api/admin/projects/{projectId}/context/{contextField}` | [docs](https://docs.getunleash.io/api) |
| [Add Or Update Legal Value For The Context Field](actions/updatecontextfieldlegalvalue.md) | `POST /api/admin/context/{contextField}/legal-values` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Add Or Update Legal Value For The Context Field](actions/updatecontextfieldlegalvalueforproject.md) | `POST /api/admin/projects/{projectId}/context/{contextField}/legal-values` | [docs](https://docs.getunleash.io/api) |
| [Updates An Environment By Name](actions/updateenvironment.md) | `PUT /api/admin/environments/update/{name}` | [docs](https://docs.getunleash.io/api) |
| [Update A Feature Flag](actions/updatefeature.md) | `PUT /api/admin/projects/{projectId}/features/{featureName}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Update A Feature Link](actions/updatefeaturelink.md) | `PUT /api/admin/projects/{projectId}/features/{featureName}/link/{linkId}` | [docs](https://docs.getunleash.io/api) |
| [Update A Strategy](actions/updatefeaturestrategy.md) | `PUT /api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies/{strategyId}` | [docs](https://docs.getunleash.io/api) |
| [Update Unleash Feedback](actions/updatefeedback.md) | `PUT /api/admin/feedback/{id}` | [docs](https://docs.getunleash.io/api) |
| [Update A Group](actions/updategroup.md) | `PUT /api/admin/groups/{groupId}` | [docs](https://docs.getunleash.io/api) |
| [Set A New Unleash License.](actions/updatelicense.md) | `POST /api/admin/license` | [docs](https://docs.getunleash.io/api) |
| [Update Project](actions/updateproject.md) | `PUT /api/admin/projects/{projectId}` | [docs](https://docs.getunleash.io/api) |
| [Updates Change Request Configuration For An Environment In The Project](actions/updateprojectchangerequestconfig.md) | `PUT /api/admin/projects/{projectId}/environments/{environment}/change-requests/config` | [docs](https://docs.getunleash.io/api) |
| [Update Project Enterprise Settings](actions/updateprojectenterprisesettings.md) | `PUT /api/admin/projects/{projectId}/settings` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Update A Milestone Strategy](actions/updateprojectmilestonestrategy.md) | `PUT /api/admin/projects/{project}/features/{featureName}/environments/{environment}/milestone-strategies/{strategyId}` | [docs](https://docs.getunleash.io/api) |
| [Update A Public Signup Token](actions/updatepublicsignuptoken.md) | `PUT /api/admin/invite-link/tokens/{token}` | [docs](https://docs.getunleash.io/api) |
| [Updates A Release Template By Its Id.](actions/updatereleasetemplate.md) | `PUT /api/admin/release-plan-templates/{templateId}` | [docs](https://docs.getunleash.io/api) |
| [Updates Existing Milestone](actions/updatereleasetemplatemilestone.md) | `PUT /api/admin/release-plan-templates/{templateId}/milestones/{milestoneId}` | [docs](https://docs.getunleash.io/api) |
| [Update A Role](actions/updaterole.md) | `PUT /api/admin/roles/{roleId}` | [docs](https://docs.getunleash.io/api) |
| [Update Segment By Id](actions/updatesegment.md) | `PUT /api/admin/segments/{id}` | [docs](https://docs.getunleash.io/api) |
| [Update A Service Account.](actions/updateserviceaccount.md) | `PUT /api/admin/service-account/{id}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Update A Signal Endpoint.](actions/updatesignalendpoint.md) | `PUT /api/admin/signal-endpoints/{id}` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Update A Signal Endpoint Token.](actions/updatesignalendpointtoken.md) | `PUT /api/admin/signal-endpoints/{signalEndpointId}/tokens/{id}` | [docs](https://docs.getunleash.io/api) |
| [Update Environment Sort Orders](actions/updatesortorder.md) | `PUT /api/admin/environments/sort-order` | [docs](https://docs.getunleash.io/api) |
| [Update Splash Settings](actions/updatesplashsettings.md) | `POST /api/admin/splash/{id}` | [docs](https://docs.getunleash.io/api) |
| [Update A Tag Type](actions/updatetagtype.md) | `PUT /api/admin/tag-types/{name}` | [docs](https://docs.getunleash.io/api) |
| [Update A User](actions/updateuser.md) | `PUT /api/admin/user-admin/{id}` | [docs](https://docs.getunleash.io/api) |
| [Validates Archive Features](actions/validatearchivefeatures.md) | `POST /api/admin/projects/{projectId}/archive/validate` | [docs](https://docs.getunleash.io/api) |
| [Validate Constraint](actions/validateconstraint.md) | `POST /api/admin/constraints/validate` | [docs](https://docs.getunleash.io/api) |
| [Validate A Context Field](actions/validatecontextfieldname.md) | `POST /api/admin/context/validate` | [docs](https://docs.getunleash.io/api) |
| [[Beta] Validate A Context Field](actions/validatecontextfieldnameforproject.md) | `POST /api/admin/projects/{projectId}/context/validate` | [docs](https://docs.getunleash.io/api) |
| [Validates If An Environment Name Exists](actions/validateenvironmentname.md) | `POST /api/admin/environments/validate` | [docs](https://docs.getunleash.io/api) |
| [Validates Password](actions/validatepassword.md) | `POST /auth/reset/validate-password` | [docs](https://docs.getunleash.io/api) |
| [Validate Project Id](actions/validateproject.md) | `POST /api/admin/projects/validate` | [docs](https://docs.getunleash.io/api) |
| [Validate Signup Token](actions/validatepublicsignuptoken.md) | `GET /invite/{token}/validate` | [docs](https://docs.getunleash.io/api) |
| [Validate A Role](actions/validaterole.md) | `POST /api/admin/roles/validate` | [docs](https://docs.getunleash.io/api) |
| [Validates If A Segment Name Exists](actions/validatesegment.md) | `POST /api/admin/segments/validate` | [docs](https://docs.getunleash.io/api) |
| [Validate A Tag Type](actions/validatetagtype.md) | `POST /api/admin/tag-types/validate` | [docs](https://docs.getunleash.io/api) |
| [Validates A Token](actions/validatetoken.md) | `GET /auth/reset/validate` | [docs](https://docs.getunleash.io/api) |
| [Validate Password For A User](actions/validateuserpassword.md) | `POST /api/admin/user-admin/validate-password` | [docs](https://docs.getunleash.io/api) |
