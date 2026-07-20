# Content Snare: Native API Reference

A consolidated summary of Content Snare's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://api.contentsnare.com/partner_api/v1/documentation
- **OpenAPI specification:** https://api.contentsnare.com/partner_api/v1/doc_data.json
- **API base URL:** `https://api.contentsnare.com`

## Authentication

### OAuth2

OAuth 2.0 authorization code flow for the Content Snare Partner API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.contentsnare.com/oauth/authorization to approve access.
2. Exchange the returned authorization code with a POST request to https://api.contentsnare.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `write_clients write_team_members write_requests review_requests read_templates read_requests read_team_members read_clients administration`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.contentsnare.com/oauth/token.

[Official authentication documentation](https://api.contentsnare.com/partner_api/v1/documentation#auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 200). Use `offset` in the query string as the record offset.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve All Submitted Fields](actions/approve-all-submitted-fields.md) | `PUT /partner_api/v1/requests/{id}/approve_all_submitted_fields` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Approve All Submitted Page Fields](actions/approve-all-submitted-page-fields.md) | `PUT /partner_api/v1/pages/{id}/approve_all_submitted_fields` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Approve All Submitted Section Fields](actions/approve-all-submitted-section-fields.md) | `PUT /partner_api/v1/sections/{id}/approve_all_submitted_fields` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Create Client](actions/create-client.md) | `POST /partner_api/v1/clients` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Create Page](actions/create-page.md) | `POST /partner_api/v1/pages` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Create Request](actions/create-request.md) | `POST /partner_api/v1/requests` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Create Section](actions/create-section.md) | `POST /partner_api/v1/sections` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Create Team Member](actions/create-team-member.md) | `POST /partner_api/v1/team_members` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Create Webhook](actions/create-webhook.md) | `POST /partner_api/v1/webhooks` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Delete Client](actions/delete-client.md) | `DELETE /partner_api/v1/clients/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Delete Request](actions/delete-request.md) | `DELETE /partner_api/v1/requests/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Delete Team Member](actions/delete-team-member.md) | `DELETE /partner_api/v1/team_members/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /partner_api/v1/webhooks/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Get Client](actions/get-client.md) | `GET /partner_api/v1/clients/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Get Page](actions/get-page.md) | `GET /partner_api/v1/pages/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Get Request](actions/get-request.md) | `GET /partner_api/v1/requests/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Get Team Member](actions/get-team-member.md) | `GET /partner_api/v1/team_members/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Get Webhook](actions/get-webhook.md) | `GET /partner_api/v1/webhooks/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [List Client Companies](actions/list-client-companies.md) | `GET /partner_api/v1/client_companies` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [List Clients](actions/list-clients.md) | `GET /partner_api/v1/clients` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [List Communications Schedules](actions/list-communications-schedules.md) | `GET /partner_api/v1/communication_templates` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [List Folders](actions/list-folders.md) | `GET /partner_api/v1/folders` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [List Page Templates](actions/list-page-templates.md) | `GET /partner_api/v1/page_templates` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [List Request Templates](actions/list-request-templates.md) | `GET /partner_api/v1/request_templates` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [List Requests](actions/list-requests.md) | `GET /partner_api/v1/requests` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [List Section Templates](actions/list-section-templates.md) | `GET /partner_api/v1/section_templates` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [List Team Members](actions/list-team-members.md) | `GET /partner_api/v1/team_members` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [List Webhooks](actions/list-webhooks.md) | `GET /partner_api/v1/webhooks` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Retrieve Current User Data](actions/retrieve-current-user-data.md) | `GET /partner_api/v1/me` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Review Request](actions/review-request.md) | `PUT /partner_api/v1/fields/{id}/review` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Run Integration Actions](actions/run-integration-actions.md) | `PUT /partner_api/v1/requests/{id}/run_integration_actions` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Submit All Fields For Review](actions/submit-all-fields-for-review.md) | `PUT /partner_api/v1/requests/{id}/submit_all_fields` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Submit All Page Fields For Review](actions/submit-all-page-fields-for-review.md) | `PUT /partner_api/v1/pages/{id}/submit_all_fields` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Submit All Section Fields For Review](actions/submit-all-section-fields-for-review.md) | `PUT /partner_api/v1/sections/{id}/submit_all_fields` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Update Client](actions/update-client.md) | `PUT /partner_api/v1/clients/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Update Request](actions/update-request.md) | `PUT /partner_api/v1/requests/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Update Team Member](actions/update-team-member.md) | `PUT /partner_api/v1/team_members/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
| [Update Webhook](actions/update-webhook.md) | `PUT /partner_api/v1/webhooks/{id}` | [docs](https://api.contentsnare.com/partner_api/v1/documentation) |
