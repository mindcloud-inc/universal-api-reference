# Queue Text Message To Bitrix Contact with LEADTEX

Queues a text message to a Bitrix contact in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendMessageToQueue?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Queue Text Message To Bitrix Contact](https://docs.leadteh.ru/rabota-s-api/rassylka/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bitrix_contact_id` | body | `number` | yes | Bitrix contact ID. |
| `text` | body | `string` | yes | Text message to queue. |
