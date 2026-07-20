# Queue Text Message with LEADTEX

Queues a text message by phone number in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendMessageToQueue?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Queue Text Message](https://docs.leadteh.ru/rabota-s-api/rassylka/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | Recipient phone number when contact IDs are not supplied. |
| `text` | body | `string` | yes | Text message to queue. |
