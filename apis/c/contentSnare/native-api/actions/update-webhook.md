# Update Webhook with Content Snare

Updates a webhook in Content Snare.

## Endpoint

- **Method:** `PUT`
- **Path:** `/partner_api/v1/webhooks/{id}`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Update Webhook](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook ID. |
| `enabled` | body | `boolean` | no | Specifies if webhook is enabled |
| `subscriptions[]` | body | `array<string>` | no | List of events associated with webhook |
| `url` | body | `string` | yes | Your webhook URL |
