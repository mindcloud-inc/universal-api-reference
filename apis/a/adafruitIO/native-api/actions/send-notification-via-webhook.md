# Send Notification via Webhook with Adafruit IO

Sends a notification to Adafruit IO via webhook.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/feed/:token/notify`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Send Notification via Webhook](https://io.adafruit.com/api/docs/#send-notification-via-webhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `token` | path | `string` | yes |
