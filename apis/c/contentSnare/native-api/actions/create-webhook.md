# Create Webhook with Content Snare

Creates a webhook in Content Snare.

## Endpoint

- **Method:** `POST`
- **Path:** `/partner_api/v1/webhooks`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Create Webhook](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | body | `boolean` | no | Specifies if webhook is enabled |
| `subscriptions[]` | body | `array<string>` | no | List of events associated with webhook |
| `url` | body | `string` | yes | Your webhook URL |
