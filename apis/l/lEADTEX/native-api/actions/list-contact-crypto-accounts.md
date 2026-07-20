# List Contact Crypto Accounts with LEADTEX

Retrieves free-form contact accounts from LEADTEX.

## Endpoint

- **Method:** `GET`
- **Path:** `/getContactCryptoAccounts?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [List Contact Crypto Accounts](https://docs.leadteh.ru/rabota-s-api/kontakty/svobodnye-scheta/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID of the contact whose crypto accounts should be returned. |
