# List Contacts with Documo

Retrieves contact records from your Documo account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [List Contacts](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | query | `string` | no | User ID. If not specified, returns results for the current user. |
| `offset` | query | `number` | no | Number of results to skip for pagination. Default 0. |
| `limit` | query | `number` | no | Number of results to return. Default 50. |
| `order` | query | `string` | no | Sort order for results. Defaults to name asc. |
| `query` | query | `string` | no | Search by contact name, fax number, phone number, or email. |
