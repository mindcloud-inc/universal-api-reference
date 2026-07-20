# Send File To Contact with LEADTEX

Sends a file message to a contact in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendMessage?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Send File To Contact](https://docs.leadteh.ru/rabota-s-api/soobsheniya/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID of the LEADTEX contact to message. |
| `file` | query | `string` | yes | URL of the file to send. |
