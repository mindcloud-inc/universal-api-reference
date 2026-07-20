# Add Funds To Contact Account with LEADTEX

Updates a contact account balance in LEADTEX by adding funds.

## Endpoint

- **Method:** `POST`
- **Path:** `/addFundsToContactAccount?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Add Funds To Contact Account](https://docs.leadteh.ru/rabota-s-api/kontakty/scheta/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `number` | yes | ID of the account to credit. |
| `amount` | body | `number` | yes | Amount in the smallest currency unit. |
| `description` | body | `string` | yes | Transaction description. |
