# Create Webhook Subscription with DitLead

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhook`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Create Webhook Subscription](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventId[]` | body | `array<string>` | no |
| `name` | body | `string` | no |
| `url` | body | `string` | no |
