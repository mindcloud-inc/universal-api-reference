# Update Webhook with CallTrackingMetrics

Updates an existing webhook in CallTrackingMetrics.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/webhooks/:webhookId`
- **Base URL:** `https://api.calltrackingmetrics.com/api/v1`
- **Official documentation:** [Update Webhook](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/7e7u819/update-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | The CallTrackingMetrics webhook ID. |
| `weburl` | body | `string` | no | The destination URL for CTM webhook delivery. |
| `hooktype` | body | `string` | no | Optional webhook trigger type. |
| `position` | body | `string` | no | The CTM webhook position enum value. |
| `name` | body | `string` | no | Optional CTM webhook display name. |
| `username` | body | `string` | no | Optional HTTP basic username CTM should send to the webhook endpoint. |
| `password` | body | `string` | no | Optional HTTP basic password CTM should send to the webhook endpoint. |
