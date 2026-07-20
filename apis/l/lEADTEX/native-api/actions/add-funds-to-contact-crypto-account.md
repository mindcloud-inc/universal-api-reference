# Add Funds To Contact Crypto Account with LEADTEX

Updates a free-form contact account in LEADTEX by adding funds.

## Endpoint

- **Method:** `POST`
- **Path:** `/addFundsToContactCryptoAccount?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Add Funds To Contact Crypto Account](https://docs.leadteh.ru/rabota-s-api/kontakty/svobodnye-scheta/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `number` | yes | ID of the crypto account to credit. |
| `amount` | body | `number` | yes | Amount to credit. |
| `description` | body | `string` | yes | Transaction description. |
