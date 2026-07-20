# Certifier: Native API Reference

A consolidated summary of Certifier's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://developers.certifier.io/docs/api-reference
- **API base URL:** `https://api.certifier.io/v1`

## Authentication

### API Key

Use a Certifier access token from your dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.certifier.io/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `pagination.next`.

## Pagination

Use `limit` in the query string to set the page size (default 20). Use `cursor` in the query string as the pagination cursor.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Credential](actions/create-credential.md) | `POST /credentials` | [docs](https://developers.certifier.io/docs/api-reference/credentials/create-a-credential) |
| [Create Credential Interaction](actions/create-credential-interaction.md) | `POST /credential-interactions` | [docs](https://developers.certifier.io/docs/api-reference/credential-interactions/create-a-credential-interaction) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://developers.certifier.io/docs/api-reference/groups/create-a-group) |
| [Create, Issue, and Send Credential](actions/create-issue-and-send-credential.md) | `POST /credentials/create-issue-send` | [docs](https://developers.certifier.io/docs/api-reference/credentials/create-issue-and-send-a-credential) |
| [Delete Credential](actions/delete-credential.md) | `DELETE /credentials/:id` | [docs](https://developers.certifier.io/docs/api-reference/credentials/list-credentials) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:id` | [docs](https://developers.certifier.io/docs/api-reference/groups/delete-a-group) |
| [Get Credential](actions/get-credential.md) | `GET /credentials/:id` | [docs](https://developers.certifier.io/docs/api-reference/credentials/get-a-credential) |
| [Get Design](actions/get-design.md) | `GET /designs/:id` | [docs](https://developers.certifier.io/docs/api-reference/designs/get-a-design) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://developers.certifier.io/docs/api-reference/groups/get-a-group) |
| [Issue Credential](actions/issue-credential.md) | `POST /credentials/:id/issue` | [docs](https://developers.certifier.io/docs/api-reference/credentials/issue-a-credential) |
| [List Attributes](actions/list-attributes.md) | `GET /attributes` | [docs](https://developers.certifier.io/docs/api-reference) |
| [List Credential Designs](actions/list-credential-designs.md) | `GET /credentials/:id/designs` | [docs](https://developers.certifier.io/docs/api-reference/credentials/get-credential-designs) |
| [List Credential Interactions](actions/list-credential-interactions.md) | `GET /credential-interactions` | [docs](https://developers.certifier.io/docs/api-reference/credential-interactions/list-credential-interactions) |
| [List Credentials](actions/list-credentials.md) | `GET /credentials` | [docs](https://developers.certifier.io/docs/api-reference/credentials/list-credentials) |
| [List Designs](actions/list-designs.md) | `GET /designs` | [docs](https://developers.certifier.io/docs/api-reference/designs/list-designs) |
| [List Email Templates](actions/list-email-templates.md) | `GET /email-templates` | [docs](https://developers.certifier.io/docs/api-reference) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://developers.certifier.io/docs/api-reference/groups/list-groups) |
| [Schedule Credential Issuance](actions/schedule-credential-issuance.md) | `POST /credentials/:id/schedule` | [docs](https://developers.certifier.io/docs/api-reference) |
| [Search Credentials](actions/search-credentials.md) | `POST /credentials/search` | [docs](https://developers.certifier.io/docs/api-reference/credentials/search-credentials) |
| [Send Credential](actions/send-credential.md) | `POST /credentials/:id/send` | [docs](https://developers.certifier.io/docs/api-reference/credentials/send-a-credential) |
| [Update Credential](actions/update-credential.md) | `PATCH /credentials/:id` | [docs](https://developers.certifier.io/docs/api-reference/credentials/update-a-credential) |
| [Update Group](actions/update-group.md) | `PATCH /groups/:id` | [docs](https://developers.certifier.io/docs/api-reference/groups/update-a-group) |
