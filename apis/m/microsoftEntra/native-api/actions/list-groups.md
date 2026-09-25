# List Groups with Microsoft Entra

## Endpoint

- **Method:** `GET`
- **Path:** `/groups`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [List Groups](https://learn.microsoft.com/en-us/graph/api/group-list?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | OData filter expression; advanced queries require Include Count. |
| `$search` | query | `string` | no | Search expression, such as "displayName:Sales"; requires Include Count. |
| `$count` | query | `boolean` | no | Required for advanced directory queries. |
| `$select` | query | `string` | no | Comma-separated group properties. |
| `$expand` | query | `string` | no | Related resources to include; incompatible with advanced queries. |
