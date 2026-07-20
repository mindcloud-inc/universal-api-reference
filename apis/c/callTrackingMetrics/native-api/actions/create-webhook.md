# Create Webhook with CallTrackingMetrics

Creates a new webhook in CallTrackingMetrics.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/webhooks`
- **Base URL:** `https://api.calltrackingmetrics.com/api/v1`
- **Official documentation:** [Create Webhook](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/0fgjrv6/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `weburl` | body | `string` | yes | The destination URL for CTM webhook delivery. |
| `hooktype` | body | `string` | no | Optional webhook trigger type. |
| `position` | body | `string` | no | The CTM webhook position enum value. |
| `name` | body | `string` | no | Optional CTM webhook display name. |
| `username` | body | `string` | no | Optional HTTP basic username CTM should send to the webhook endpoint. |
| `password` | body | `string` | no | Optional HTTP basic password CTM should send to the webhook endpoint. |
