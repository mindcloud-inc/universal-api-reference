# Create Contact Crypto Account with LEADTEX

Creates a free-form contact account in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/addContactCryptoAccount?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Create Contact Crypto Account](https://docs.leadteh.ru/rabota-s-api/kontakty/svobodnye-scheta/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | ID of the contact to create the crypto account for. |
| `currency` | body | `string` | yes | Crypto currency code, such as BTC. |
