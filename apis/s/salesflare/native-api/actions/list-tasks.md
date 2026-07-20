# List Tasks with Salesflare

## Endpoint

- **Method:** `GET`
- **Path:** `tasks`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [List Tasks](https://api.salesflare.com/docs#/Tasks/getTasks)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of tasks to return. |
| `order_by` | query | `string` | no | Sort expression such as due_date desc. |
| `search` | query | `string` | no | Free-text search across tasks. |
| `offset` | query | `number` | no | Number of tasks to skip before returning results. |
