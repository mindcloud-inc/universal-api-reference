# Send Arbitrary Data via Webhook with Adafruit IO

Sends raw feed data to Adafruit IO via webhook.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/feed/:token/raw`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Send Arbitrary Data via Webhook](https://io.adafruit.com/api/docs/#send-arbitrary-data-via-webhook)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/plain` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `body` | body | `string` | yes |
| `token` | path | `string` | yes |
