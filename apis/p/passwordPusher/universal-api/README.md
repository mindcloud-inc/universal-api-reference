# <img src="https://images.mindcloud.co/apps/icons/password-pusher_1776349070617.png" alt="Password Pusher logo" width="28" height="28"> Password Pusher: Universal API

Create, retrieve, audit, and manage secure one-way pushes and two-way sensitive-information requests with Password Pusher API v2.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/passwordPusher/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://eu.pwpush.com
- **Vendor API docs:** https://eu.pwpush.com/help/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves a list of workspaces from Password Pusher. |

### Api Version

| Action | Method | Description |
| --- | --- | --- |
| [Get API Version](actions/get-api-version.md) | GET | Retrieves API version and feature details from Password Pusher. |

### Push

| Action | Method | Description |
| --- | --- | --- |
| [Create Push](actions/create-push.md) | POST | Creates a secure push in Password Pusher. |
| [Expire Push](actions/expire-push.md) | DELETE | Expires an existing push in Password Pusher. |
| [List Active Pushes](actions/list-active-pushes.md) | GET | Retrieves active pushes from Password Pusher. |
| [List Expired Pushes](actions/list-expired-pushes.md) | GET | Retrieves expired pushes from Password Pusher. |
| [Retrieve Push](actions/retrieve-push.md) | GET | Retrieves a push payload from Password Pusher. |

### Push Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Push Audit Log](actions/get-push-audit-log.md) | GET | Retrieves a push audit log from Password Pusher. |

### Push Preview

| Action | Method | Description |
| --- | --- | --- |
| [Preview Push](actions/preview-push.md) | GET | Retrieves a push URL preview from Password Pusher. |

### Request

| Action | Method | Description |
| --- | --- | --- |
| [Close Request](actions/close-request.md) | DELETE | Closes an existing request in Password Pusher. |
| [Create Request](actions/create-request.md) | POST | Creates a secure request in Password Pusher. |
| [List Active Requests](actions/list-active-requests.md) | GET | Retrieves active requests from Password Pusher. |
| [List Closed Requests](actions/list-closed-requests.md) | GET | Retrieves closed requests from Password Pusher. |
| [List Open Requests](actions/list-open-requests.md) | GET | Retrieves open requests from Password Pusher. |
| [List Ready Requests](actions/list-ready-requests.md) | GET | Retrieves ready requests from Password Pusher. |
| [Retrieve Request](actions/retrieve-request.md) | GET | Retrieves a request response from Password Pusher. |

### Request Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Request Audit Log](actions/get-request-audit-log.md) | GET | Retrieves a request audit log from Password Pusher. |

### Request Preview

| Action | Method | Description |
| --- | --- | --- |
| [Preview Request](actions/preview-request.md) | GET | Retrieves a request URL preview from Password Pusher. |

### Request Response

| Action | Method | Description |
| --- | --- | --- |
| [Respond To Request](actions/respond-to-request.md) | PUT | Responds to an open request in Password Pusher. |

