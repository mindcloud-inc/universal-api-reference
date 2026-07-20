# Get Single Chat with WhatsBoost

Retrieves a chat by ID from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/get/wa.message`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Get Single Chat](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | The ID of the WhatsApp message |
| `type` | body | `string` | yes | The message type to query: <code>sent</code> or <code>received</code> |
