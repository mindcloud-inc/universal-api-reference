# Get message by ID with Bulldog-WP

Retrieves a message from Bulldog-WP.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/{messageId}`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [Get message by ID](https://console.bulldog-wp.co.il/docs/specification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Outbound message ID or WhatsApp message ID. |
