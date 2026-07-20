# Delete Contact Variable By ID with LEADTEX

Deletes a contact variable from LEADTEX by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteContactVariable?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Delete Contact Variable By ID](https://docs.leadteh.ru/rabota-s-api/kontakty/polzovatelskie-peremennye/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID of the contact variable record. |
| `id` | query | `number` | yes | ID of the variable to delete. |
