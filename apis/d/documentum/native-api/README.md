# Documentum: Native API Reference

A consolidated summary of Documentum's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://opentext.github.io/d2sv-sdk/23.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf
- **API base URL:** `{documentumRestBaseUrl}`

## Authentication

### OAuth2

OpenText OAuth2 bearer-token authentication. Documentum deployments may use instance-specific OTDS or Developer Cloud token endpoints.

### Credentials

- **Documentum REST base URL:** `documentumRestBaseUrl` · required · Base URL for the target Documentum REST/D2FS service, for example https://host.example.com/d2fs-rest or https://host.example.com/dctm-rest.
- **OAuth token URL:** `oauthTokenUrl` · required · Exact OpenText/OTDS OAuth2 token endpoint for this deployment.
- **Client ID:** `clientId` · required · Confidential OAuth client ID for the OpenText application.
- **Client secret:** `clientSecret` · required · Confidential OAuth client secret for the OpenText application.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to {{credentials.oauthTokenUrl}}.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://www.postman.com/opentext-devcloud/opentext-developer-cloud-public-resources/folder/18209070-a567812f-a7ac-4d53-8767-ab11d135f5f3)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Lifecycle State](actions/apply-lifecycle-state.md) | `PUT /repositories/{repositoryName}/d2-objects-lifecycle-state` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Apply Template To Object](actions/apply-template-to-object.md) | `POST /repositories/{repositoryName}/objects-d2/{objectId}` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Check In Object Version](actions/check-in-object-version.md) | `POST /repositories/{repositoryName}/objects/{chronicleId}/versions` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Create D2 Object](actions/create-d2-object.md) | `POST /repositories/{repositoryName}/object-creation` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Export Object Audit](actions/export-object-audit.md) | `GET /repositories/{repositoryName}/objects/{objectId}/audit-export` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Export Object Locations](actions/export-object-locations.md) | `GET /repositories/{repositoryName}/objects/{objectId}/locations-export` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Get Audit Trail Event Source Facets](actions/get-audit-trail-event-source-facets.md) | `GET /repositories/{repositoryName}/objects/{objectId}/audit-trail-facets-by-event-source` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Get Audit Trail Relative Date Facets](actions/get-audit-trail-relative-date-facets.md) | `GET /repositories/{repositoryName}/objects/{objectId}/audit-trail-facets-by-relative-date` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Get Creation Profile](actions/get-creation-profile.md) | `GET /repositories/{repositoryName}/profile-configuration/{profileId}` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Get D2 Type](actions/get-d2-type.md) | `GET /repositories/{repositoryName}/type-configuration/{typeId}` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Get Encrypted DM Ticket](actions/get-encrypted-dm-ticket.md) | `GET /repositories/{repositoryName}/dm-ticket` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Get Native Annotations](actions/get-native-annotations.md) | `GET /repositories/{repositoryName}/objects/{objectId}/native-annotations-for-collaboration-edit` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Get Search Configuration](actions/get-search-configuration.md) | `GET /repositories/{repositoryName}/search-configuration/{configId}` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Get Workflow Report Tasks](actions/get-workflow-report-tasks.md) | `GET /repositories/{repositoryName}/d2-workflows/{workflowId}/d2-report-tasks` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Get Workflow Task Status](actions/get-workflow-task-status.md) | `GET /repositories/{repositoryName}/processes/{processName}/{processId}/{taskName}/{taskId}/status` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [List C2 Print URLs](actions/list-c2-print-urls.md) | `GET /repositories/{repositoryName}/objects/{objectId}/views/c2-print` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [List C2 View URLs](actions/list-c2-view-urls.md) | `GET /repositories/{repositoryName}/objects/{objectId}/views/c2-view` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [List Creation Profiles](actions/list-creation-profiles.md) | `GET /repositories/{repositoryName}/profile-configuration` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [List D2 Types](actions/list-d2-types.md) | `GET /repositories/{repositoryName}/type-configuration` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [List Document Templates](actions/list-document-templates.md) | `GET /repositories/{repositoryName}/objects/{objectId}/document-templates` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [List Preview URLs](actions/list-preview-urls.md) | `GET /repositories/{repositoryName}/objects/{objectId}/preview-urls-d2` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [List Repositories](actions/list-repositories.md) | `GET /repositories` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [List Search Configurations](actions/list-search-configurations.md) | `GET /repositories/{repositoryName}/search-configuration` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [List Workflow Tasks](actions/list-workflow-tasks.md) | `GET /repositories/{repositoryName}/tasklist` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Run Query Form Search](actions/run-query-form-search.md) | `POST /repositories/{repositoryName}/d2-saved-searches/queryforms/{queryFormId}/results` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Run Quick Search](actions/run-quick-search.md) | `POST /repositories/{repositoryName}/quickSearch` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Update Workflow Task Notes](actions/update-workflow-task-notes.md) | `PUT /repositories/{repositoryName}/processes/{processName}/{processId}/{taskName}/{taskId}/notes` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
| [Update Workflow Task Status](actions/update-workflow-task-status.md) | `POST /repositories/{repositoryName}/processes/{processName}/{processId}/{taskName}/{taskId}/status` | [docs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf) |
