# Send Data via Webhook with Adafruit IO

Creates a data point in Adafruit IO via webhook.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/feed/:token`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Send Data via Webhook](https://io.adafruit.com/api/docs/#send-data-via-webhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ele` | body | `number` | no |
| `lat` | body | `number` | no |
| `lon` | body | `number` | no |
| `token` | path | `string` | yes |
| `value` | body | `string` | yes |
