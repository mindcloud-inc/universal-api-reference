# Create Webhook with Underdog Protocol

Creates a new webhook in Underdog Protocol.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/webhooks`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Create Webhook](https://docs.underdogprotocol.com/resources/webhooks/create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Encoded URL for the callback endpoint. |
| `triggers[]` | body | `array<string>` | yes | — |
