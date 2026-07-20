# Delete Contact Account with LEADTEX

Deletes an ISO 4217 contact account from LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteContactAccount?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Delete Contact Account](https://docs.leadteh.ru/rabota-s-api/kontakty/scheta/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `number` | yes | ID of the account to delete. |
