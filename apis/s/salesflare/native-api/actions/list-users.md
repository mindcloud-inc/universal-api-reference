# List Users with Salesflare

## Endpoint

- **Method:** `GET`
- **Path:** `users`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [List Users](https://api.salesflare.com/docs#/Users/getUsers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of users to return. |
| `order_by` | query | `string` | no | Sort expression such as name desc. |
| `search` | query | `string` | no | Free-text search across users. |
| `offset` | query | `number` | no | Number of users to skip before returning results. |
