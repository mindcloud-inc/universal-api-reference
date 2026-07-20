# Create Webhook with RAYNET CRM

## Endpoint

- **Method:** `PUT`
- **Path:** `webhook/`
- **Base URL:** `https://app.raynetcrm.com/api/v2/`
- **Official documentation:** [Create Webhook](https://app.raynetcrm.com/api/doc/index-en.html#tag/Webhook/operation/webhookInsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes | Webhook events array. |
| `secretToken` | body | `string` | no | Webhook secret token. |
| `url` | body | `string` | yes | Webhook destination URL. |
