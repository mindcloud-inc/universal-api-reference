# Update Webhook with CircleCI

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhook/:webhook_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Update Webhook](https://circleci.com/docs/api/v2/#tag/Webhook/operation/updateWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events` | body | `string` | no | Events that should trigger this webhook. |
| `name` | body | `string` | no | Webhook display name. |
| `signing-secret` | body | `string` | no | Secret used to sign webhook payloads. |
| `url` | body | `string` | no | Destination URL for webhook deliveries. |
| `verify-tls` | body | `string` | no | Whether CircleCI should verify the server certificate. |
| `webhook_id` | path | `string` | yes | Opaque webhook identifier. |
