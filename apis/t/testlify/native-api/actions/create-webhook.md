# Create Webhook with Testlify

Creates a webhook subscription in Testlify.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhook`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [Create Webhook](https://docs.testlify.com/reference/create_webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Webhook name. |
| `payloadUrl` | body | `string` | yes | Webhook destination URL. |
| `events[]` | body | `array<string>` | yes | Webhook event names. |
