# SpreadsheetWeb Hub: Native API Reference

A consolidated summary of SpreadsheetWeb Hub's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.spreadsheetweb.com/index.html
- **OpenAPI specification:** https://api.spreadsheetweb.com/swagger/v3/swagger.json
- **API base URL:** `https://api.spreadsheetweb.com`

## Authentication

### OAuth2

### Credentials

- **Client ID:** `clientId` · required · SpreadsheetWeb Hub API client identifier.
- **Client Secret:** `clientSecret` · required · SpreadsheetWeb Hub API client secret.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://identity.spreadsheetweb.com/connect/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://identity.spreadsheetweb.com/connect/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `pagos_hub_api`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://help.spreadsheetweb.com/hub/web-services/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the request body to set the page size. Use `pageIndex` in the request body to choose the page.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Multiple](actions/calculate-multiple.md) | `POST /calculations/calculatemultiple` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Calculate Multiple Async](actions/calculate-multiple-async.md) | `POST /calculations/calculatemultipleasync` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Calculate Single](actions/calculate-single.md) | `POST /calculations/calculatesingle` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Calculate Single Simple](actions/calculate-single-simple.md) | `POST /calculations/calculatesinglesimple` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Create Data Share Link](actions/create-data-share-link.md) | `POST /datashare/create` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Create Tag](actions/create-tag.md) | `POST /tags/create` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Create Workspace Invite](actions/create-workspace-invite.md) | `POST /invites/create` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Delete Data Share Link](actions/delete-data-share-link.md) | `POST /datashare/delete` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Delete Tag](actions/delete-tag.md) | `POST /tags/delete` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Get Application](actions/get-application.md) | `GET /applications/get/:applicationId/:workspaceId` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Get Application by Slug](actions/get-application-by-slug.md) | `GET /applications/getbyslug/:applicationSlug/:workspaceId` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Get Calculation Progress](actions/get-calculation-progress.md) | `POST /calculations/getprogressstate` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Get Tag](actions/get-tag.md) | `GET /tags/get/:tagId/:workspaceId` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Get User](actions/get-user.md) | `GET /users/get/:workspaceId/:userId` | [docs](https://api.spreadsheetweb.com/index.html) |
| [List Application Tag Relationships](actions/list-application-tag-relationships.md) | `GET /applications/gettagrelationships/:applicationId/:workspaceId` | [docs](https://api.spreadsheetweb.com/index.html) |
| [List Applications](actions/list-applications.md) | `POST /applications/list/:workspaceId/:onlyPublishedWithDatabases` | [docs](https://api.spreadsheetweb.com/index.html) |
| [List Applications by IDs](actions/list-applications-by-ids.md) | `POST /applications/getmany` | [docs](https://api.spreadsheetweb.com/index.html) |
| [List Data Share Links](actions/list-data-share-links.md) | `POST /datashare/list/:workspaceId/:applicationId/:dataId` | [docs](https://api.spreadsheetweb.com/index.html) |
| [List Tags](actions/list-tags.md) | `POST /tags/list/:workspaceId` | [docs](https://api.spreadsheetweb.com/index.html) |
| [List Users](actions/list-users.md) | `POST /users/list/:workspaceId` | [docs](https://api.spreadsheetweb.com/index.html) |
| [List Workspace Invites](actions/list-workspace-invites.md) | `POST /invites/workspacelist/:workspaceId` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Prepopulate Instance](actions/prepopulate-instance.md) | `POST /calculations/prepopulateinstance` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Update Data Share Link](actions/update-data-share-link.md) | `POST /datashare/update` | [docs](https://api.spreadsheetweb.com/index.html) |
| [Update Tag](actions/update-tag.md) | `POST /tags/edit` | [docs](https://api.spreadsheetweb.com/index.html) |
