# List Contact Accounts with LEADTEX

Retrieves ISO 4217 contact accounts from LEADTEX.

## Endpoint

- **Method:** `GET`
- **Path:** `/getContactAccounts?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [List Contact Accounts](https://docs.leadteh.ru/rabota-s-api/kontakty/scheta/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID of the contact whose accounts should be returned. |
