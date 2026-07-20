# Create Webhook Subscription with PresEngage

Creates a new webhook subscription in PresEngage.

## Endpoint

- **Method:** `POST`
- **Path:** `/hooks`
- **Base URL:** `https://shared.presengage.com/functions/v1/presengage-api`
- **Official documentation:** [Create Webhook Subscription](https://developer.presengage.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | body | `string` | yes | Webhook URL that should receive PresEngage notifications. |
