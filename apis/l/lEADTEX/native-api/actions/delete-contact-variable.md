# Delete Contact Variable with LEADTEX

Deletes a contact variable from LEADTEX by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteContactVariable?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Delete Contact Variable](https://docs.leadteh.ru/rabota-s-api/kontakty/polzovatelskie-peremennye/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID of the contact variable record. |
| `name` | query | `string` | yes | Variable name to delete when ID is not supplied. |
