# Withdraw Funds From Contact Account with LEADTEX

Updates a contact account balance in LEADTEX by withdrawing funds.

## Endpoint

- **Method:** `POST`
- **Path:** `/withdrawFundsFromContactAccount?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Withdraw Funds From Contact Account](https://docs.leadteh.ru/rabota-s-api/kontakty/scheta/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `number` | yes | ID of the account to debit. |
| `amount` | body | `number` | yes | Amount in the smallest currency unit. |
| `description` | body | `string` | yes | Transaction description. |
