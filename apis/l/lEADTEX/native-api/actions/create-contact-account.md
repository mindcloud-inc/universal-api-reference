# Create Contact Account with LEADTEX

Creates an ISO 4217 contact account in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/addContactAccount?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Create Contact Account](https://docs.leadteh.ru/rabota-s-api/kontakty/scheta/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | ID of the contact to create the account for. |
| `currency` | body | `string` | yes | Three-letter ISO 4217 currency code, such as USD. |
