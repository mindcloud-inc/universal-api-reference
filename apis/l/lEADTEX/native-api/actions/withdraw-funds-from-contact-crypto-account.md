# Withdraw Funds From Contact Crypto Account with LEADTEX

Updates a free-form contact account in LEADTEX by withdrawing funds.

## Endpoint

- **Method:** `POST`
- **Path:** `/withdrawFundsFromContactCryptoAccount?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Withdraw Funds From Contact Crypto Account](https://docs.leadteh.ru/rabota-s-api/kontakty/svobodnye-scheta/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `number` | yes | ID of the crypto account to debit. |
| `amount` | body | `number` | yes | Amount to debit. |
| `description` | body | `string` | yes | Transaction description. |
