# List Contacts With Details with LEADTEX

Retrieves contacts with related details from LEADTEX.

## Endpoint

- **Method:** `GET`
- **Path:** `/getContacts?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [List Contacts With Details](https://docs.leadteh.ru/rabota-s-api/kontakty/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `with` | query | `string` | yes | Additional contact entities to include. Use tags,variables for this action. |
