# Create Webhook with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Create Webhook](https://circleci.com/docs/api/v2/#tag/Webhook/operation/createWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes | Events that should trigger this webhook. |
| `name` | body | `string` | yes | Webhook display name. |
| `scope` | body | `object` | yes | Webhook scope configuration. |
| `signing-secret` | body | `string` | no | Secret used to sign webhook payloads. |
| `url` | body | `string` | yes | Destination URL for webhook deliveries. |
| `verify-tls` | body | `boolean` | no | Whether CircleCI should verify the server certificate. |
