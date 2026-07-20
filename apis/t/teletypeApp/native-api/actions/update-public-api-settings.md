# Update Public API Settings with Teletype App

Updates public API settings in Teletype App.

## Endpoint

- **Method:** `POST`
- **Path:** `/project/update-public-api`
- **Base URL:** `https://api.teletype.app/public/api/v1`
- **Official documentation:** [Update Public API Settings](https://teletype.app/help/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_webhook` | body | `string` | no | Webhook URL to store in the Teletype project public API settings. |
| `active_webhooks[]` | body | `array<string>` | no | Webhook event names to enable for the Teletype project public API settings. |
