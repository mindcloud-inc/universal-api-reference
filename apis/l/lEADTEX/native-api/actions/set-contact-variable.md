# Set Contact Variable with LEADTEX

Creates or updates a contact variable in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/setContactVariable?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Set Contact Variable](https://docs.leadteh.ru/rabota-s-api/kontakty/polzovatelskie-peremennye/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID of the contact whose variable should be set. |
| `name` | query | `string` | yes | Variable name. |
| `value` | query | `string` | yes | Variable value. |
