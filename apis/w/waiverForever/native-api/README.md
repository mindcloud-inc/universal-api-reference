# WaiverForever: Native API Reference

A consolidated summary of WaiverForever's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.waiverforever.com/
- **API base URL:** `https://api.waiverforever.com`

## Authentication

### API Key

Connect with your WaiverForever application key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.waiverforever.com/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Waiver](actions/accept-waiver.md) | `POST /openapi/v2/waiver/:waiver_id/accept` | [docs](https://docs.waiverforever.com/#accept-waiver) |
| [Create Waiver Request](actions/create-waiver-request.md) | `POST /openapi/v2/waiverRequest` | [docs](https://docs.waiverforever.com/#create-waiver-request) |
| [Edit Waiver Request](actions/edit-waiver-request.md) | `POST /openapi/v2/waiverRequest/:waiver_request_id` | [docs](https://docs.waiverforever.com/#edit-waiver-request) |
| [Generate Template Prefill Link](actions/generate-template-prefill-link.md) | `POST /openapi/v2/template/:template_id/prefill` | [docs](https://docs.waiverforever.com/#generate-template-prefill-link) |
| [Get Sample Waiver](actions/get-sample-waiver.md) | `GET /openapi/v1/template/:template_id/getSampleWaiver` | [docs](https://docs.waiverforever.com/#get-sample-waiver) |
| [Get Signed Waiver](actions/get-signed-waiver.md) | `GET /openapi/v1/waiver/:waiver_id` | [docs](https://docs.waiverforever.com/#get-signed-waiver) |
| [Get Template Prefill Schema](actions/get-template-prefill-schema.md) | `GET /openapi/v2/template/:template_id/prefill/schema` | [docs](https://docs.waiverforever.com/#get-template-prefill-schema) |
| [Get Tracking Waiver](actions/get-tracking-waiver.md) | `GET /openapi/v1/waiver/tracking/:tracking_id` | [docs](https://docs.waiverforever.com/#get-tracking-waiver) |
| [Get User Info](actions/get-user-info.md) | `GET /openapi/v1/auth/userInfo` | [docs](https://docs.waiverforever.com/#get-user-info) |
| [Get Waiver Request](actions/get-waiver-request.md) | `GET /openapi/v2/waiverRequest/:waiver_request_id` | [docs](https://docs.waiverforever.com/#get-waiver-request) |
| [Get Waiver Request Prefill Schema](actions/get-waiver-request-prefill-schema.md) | `GET /openapi/v2/waiverRequest/:group_id/prefill/schema` | [docs](https://docs.waiverforever.com/#get-waiver-request-prefill-schema) |
| [Get Waiver Request Tracking Info](actions/get-waiver-request-tracking-info.md) | `GET /openapi/v2/waiverRequests/groupTrackings` | [docs](https://docs.waiverforever.com/#get-waiver-request-tracking-info) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /openapi/v1/webhooks/` | [docs](https://docs.waiverforever.com/#get-all-subscriptions) |
| [List Templates](actions/list-templates.md) | `GET /openapi/v1/templates` | [docs](https://docs.waiverforever.com/#get-template-list) |
| [List Waiver Requests](actions/list-waiver-requests.md) | `GET /openapi/v2/waiverRequests` | [docs](https://docs.waiverforever.com/#list-waiver-requests) |
| [Request Waiver](actions/request-waiver.md) | `GET /openapi/v1/template/:template_id/requestWaiver` | [docs](https://docs.waiverforever.com/#request-waiver) |
| [Search Waivers](actions/search-waivers.md) | `POST /openapi/v1/waiver/search` | [docs](https://docs.waiverforever.com/#waiver-search) |
| [Send Requests via Email](actions/send-requests-via-email.md) | `POST /openapi/v2/waiverRequests/sendGroupEmail` | [docs](https://docs.waiverforever.com/#send-requests-via-email) |
| [Subscribe an Event](actions/subscribe-an-event.md) | `POST /openapi/v1/webhooks/` | [docs](https://docs.waiverforever.com/#subscribe-an-event) |
| [Unsubscribe an Event](actions/unsubscribe-an-event.md) | `DELETE /openapi/v1/webhooks/:subscription_id/` | [docs](https://docs.waiverforever.com/#unsubscribe-an-event) |
| [Update Waiver Note](actions/update-waiver-note.md) | `POST /openapi/v1/waiver/:waiver_id/note` | [docs](https://docs.waiverforever.com/#update-waiver-note) |
