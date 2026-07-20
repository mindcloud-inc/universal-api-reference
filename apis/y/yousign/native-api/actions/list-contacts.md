# List Contacts with Yousign

Retrieves contacts from Yousign.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [List Contacts](https://developers.yousign.com/reference/get-contacts-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Return contacts after this pagination cursor. |
| `limit` | query | `number` | no | Maximum number of contacts to return. |
