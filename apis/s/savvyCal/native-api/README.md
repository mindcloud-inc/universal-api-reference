# SavvyCal: Native API Reference

A consolidated summary of SavvyCal's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://developers.savvycal.com/category/rest-api
- **API base URL:** `https://api.savvycal.com`

## Authentication

### OAuth 2.0

Connect SavvyCal with OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://savvycal.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://savvycal.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://savvycal.com/oauth/token.

[Official authentication documentation](https://developers.savvycal.com/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `data.metadata.after`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `after` in the query string as the pagination cursor; numbering starts at 1.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Event](actions/cancel-event.md) | `POST /v1/events/:event_id/cancel` | [docs](https://developers.savvycal.com/api/cancel-event) |
| [Create Event](actions/create-event.md) | `POST /v1/links/:link_id/events` | [docs](https://developers.savvycal.com/api/create-event) |
| [Create Personal Scheduling Link](actions/create-personal-scheduling-link.md) | `POST /v1/links` | [docs](https://developers.savvycal.com/api/create-personal-scheduling-link) |
| [Create Scope Scheduling Link](actions/create-scope-scheduling-link.md) | `POST /v1/scopes/:scope_slug/links` | [docs](https://developers.savvycal.com/api/create-scope-scheduling-link) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/webhooks` | [docs](https://developers.savvycal.com/api/create-webhook) |
| [Delete Scheduling Link](actions/delete-scheduling-link.md) | `DELETE /v1/links/:link_id` | [docs](https://developers.savvycal.com/api/delete-scheduling-link) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/webhooks/:webhook_id` | [docs](https://developers.savvycal.com/api/delete-webhook) |
| [Duplicate Scheduling Link](actions/duplicate-scheduling-link.md) | `POST /v1/links/:link_id/duplicate` | [docs](https://developers.savvycal.com/api/duplicate-scheduling-link) |
| [Get Current User](actions/get-current-user.md) | `GET /v1/me` | [docs](https://developers.savvycal.com/api/get-current-user) |
| [Get Event](actions/get-event.md) | `GET /v1/events/:event_id` | [docs](https://developers.savvycal.com/api/get-event) |
| [Get Scheduling Link](actions/get-scheduling-link.md) | `GET /v1/links/:link_id` | [docs](https://developers.savvycal.com/api/get-scheduling-link) |
| [Get Time Zone](actions/get-time-zone.md) | `GET /v1/time_zones/:segments` | [docs](https://developers.savvycal.com/api/get-time-zone) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/webhooks/:webhook_id` | [docs](https://developers.savvycal.com/api/get-webhook) |
| [List Available Time Slots](actions/list-available-time-slots.md) | `GET /v1/links/:link_id/slots` | [docs](https://developers.savvycal.com/api/get-link-slots) |
| [List Events](actions/list-events.md) | `GET /v1/events` | [docs](https://developers.savvycal.com/api/list-events) |
| [List Scheduling Links](actions/list-scheduling-links.md) | `GET /v1/links` | [docs](https://developers.savvycal.com/api/list-scheduling-links) |
| [List Time Zones](actions/list-time-zones.md) | `GET /v1/time_zones` | [docs](https://developers.savvycal.com/api/list-time-zones) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://developers.savvycal.com/api/list-webhooks) |
| [List Workflow Rules](actions/list-workflow-rules.md) | `GET /v1/workflows/:workflow_id/rules` | [docs](https://developers.savvycal.com/api/list-workflow-rules) |
| [List Workflows](actions/list-workflows.md) | `GET /v1/workflows` | [docs](https://developers.savvycal.com/api/list-workflows) |
| [Toggle Scheduling Link](actions/toggle-scheduling-link.md) | `POST /v1/links/:link_id/toggle` | [docs](https://developers.savvycal.com/api/toggle-scheduling-link) |
| [Update Scheduling Link](actions/update-scheduling-link.md) | `PATCH /v1/links/:link_id` | [docs](https://developers.savvycal.com/api/update-scheduling-link) |
