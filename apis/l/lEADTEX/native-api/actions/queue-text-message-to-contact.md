# Queue Text Message To Contact with LEADTEX

Queues a text message to a contact in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendMessageToQueue?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Queue Text Message To Contact](https://docs.leadteh.ru/rabota-s-api/rassylka/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | LEADTEX contact ID. |
| `text` | body | `string` | yes | Text message to queue. |
