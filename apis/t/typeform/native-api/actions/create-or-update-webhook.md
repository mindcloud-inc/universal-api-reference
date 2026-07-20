# Create or Update Webhook with Typeform

## Endpoint

- **Method:** `PUT`
- **Path:** `/forms/:formId/webhooks/:tag`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Create or Update Webhook](https://www.typeform.com/developers/webhooks/reference/create-or-update-webhook/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | body | `boolean` | no | Whether webhook delivery is enabled. |
| `event_types` | body | `object` | no | Webhook event types configuration. |
| `formId` | path | `string` | yes | Typeform form identifier. |
| `secret` | body | `string` | no | Webhook signing secret. |
| `tag` | path | `string` | yes | Webhook tag. |
| `url` | body | `string` | no | Destination URL for webhook deliveries. |
| `verify_ssl` | body | `boolean` | no | Whether SSL certificate verification is enabled. |
