# List Contacts with Salesflare

## Endpoint

- **Method:** `GET`
- **Path:** `contacts`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [List Contacts](https://api.salesflare.com/docs#/Contacts/getContacts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of contacts to return. |
| `offset` | query | `number` | no | Number of contacts to skip before returning results. |
| `order_by` | query | `string` | no | Sort expression such as name or creation_date desc. |
| `search` | query | `string` | no | Free-text search across contacts. |
