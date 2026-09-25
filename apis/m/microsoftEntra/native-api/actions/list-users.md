# List Users with Microsoft Entra

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [List Users](https://learn.microsoft.com/en-us/graph/api/user-list?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | OData filter expression. Advanced queries require Include Count. |
| `$search` | query | `string` | no | Search expression, such as "displayName:Ava". Requires Include Count. |
| `$count` | query | `boolean` | no | Include the matching count. Required for advanced search, filtering, and sorting. |
| `$select` | query | `string` | no | Comma-separated properties, such as id,displayName. |
| `$expand` | query | `string` | no | Related resources to include. Advanced directory queries do not support expand. |
