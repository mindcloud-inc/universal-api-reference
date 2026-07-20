# Get Single Message with WhatsBoost

Retrieves a message by ID from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/get/sms.message`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Get Single Message](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | The ID of the SMS message |
| `type` | body | `string` | yes | The message type to query: <code>sent</code> or <code>received</code> |
