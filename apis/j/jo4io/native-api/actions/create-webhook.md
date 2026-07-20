# Create Webhook with jo4.io

## Endpoint

- **Method:** `POST`
- **Path:** `/protected/webhooks`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Create Webhook](https://jo4-api.jo4.io/swagger-ui/index.html#/webhook-controller/createWebhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `events` | body | `string` | no |
| `name` | body | `string` | yes |
| `url` | body | `string` | yes |
