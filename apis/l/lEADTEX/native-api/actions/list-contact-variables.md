# List Contact Variables with LEADTEX

Retrieves custom variables for a specific contact in LEADTEX.

## Endpoint

- **Method:** `GET`
- **Path:** `/getContactVariables?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [List Contact Variables](https://docs.leadteh.ru/rabota-s-api/kontakty/polzovatelskie-peremennye/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID of the contact whose variables should be returned. |
