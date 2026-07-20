# <img src="https://images.mindcloud.co/apps/icons/waiver_1774028429747.png" alt="WaiverForever logo" width="28" height="28"> WaiverForever: Universal API

Create, sign, and manage digital waivers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/waiverForever/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.waiverforever.com
- **Vendor API docs:** https://docs.waiverforever.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from WaiverForever. |
| [Request Waiver](actions/request-waiver.md) | POST | Creates a waiver request link from a WaiverForever template. |

### Template Prefill Link

| Action | Method | Description |
| --- | --- | --- |
| [Generate Template Prefill Link](actions/generate-template-prefill-link.md) | POST | Creates a prefilled template link in WaiverForever. |

### Template Prefill Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Prefill Schema](actions/get-template-prefill-schema.md) | GET | Retrieves a template prefill schema from WaiverForever. |

### Template Sample Waiver

| Action | Method | Description |
| --- | --- | --- |
| [Get Sample Waiver](actions/get-sample-waiver.md) | GET | Retrieves a sample waiver from a WaiverForever template. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves user info from WaiverForever. |

### Waiver

| Action | Method | Description |
| --- | --- | --- |
| [Accept Waiver](actions/accept-waiver.md) | PUT | Accepts a waiver in WaiverForever. |
| [Get Signed Waiver](actions/get-signed-waiver.md) | GET | Retrieves a signed waiver from WaiverForever. |
| [Get Tracking Waiver](actions/get-tracking-waiver.md) | GET | Retrieves a waiver from WaiverForever by tracking ID. |
| [Update Waiver Note](actions/update-waiver-note.md) | PUT | Updates a waiver note in WaiverForever. |

### Waiver Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Waiver Request](actions/create-waiver-request.md) | POST | Creates a waiver request in WaiverForever. |
| [Edit Waiver Request](actions/edit-waiver-request.md) | PUT | Updates a waiver request in WaiverForever. |
| [Get Waiver Request](actions/get-waiver-request.md) | GET | Retrieves a waiver request from WaiverForever. |
| [List Waiver Requests](actions/list-waiver-requests.md) | GET | Retrieves waiver requests from WaiverForever. |

### Waiver Request Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Requests via Email](actions/send-requests-via-email.md) | POST | Sends waiver requests by email from WaiverForever. |

### Waiver Request Prefill Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Waiver Request Prefill Schema](actions/get-waiver-request-prefill-schema.md) | GET | Retrieves a waiver request prefill schema from WaiverForever. |

### Waiver Request Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Get Waiver Request Tracking Info](actions/get-waiver-request-tracking-info.md) | GET | Retrieves waiver request tracking info from WaiverForever. |

### Waiver Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Waivers](actions/search-waivers.md) | GET | Finds waivers in WaiverForever by search criteria. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves webhook subscriptions from WaiverForever. |
| [Subscribe an Event](actions/subscribe-an-event.md) | POST | Creates a webhook subscription in WaiverForever. |
| [Unsubscribe an Event](actions/unsubscribe-an-event.md) | DELETE | Deletes a webhook subscription from WaiverForever. |

