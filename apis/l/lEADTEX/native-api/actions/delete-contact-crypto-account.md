# Delete Contact Crypto Account with LEADTEX

Deletes a free-form contact account from LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteContactCryptoAccount?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Delete Contact Crypto Account](https://docs.leadteh.ru/rabota-s-api/kontakty/svobodnye-scheta/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `number` | yes | ID of the crypto account to delete. |
