# List columns with YouGile

Retrieves a list of columns from YouGile.

## Endpoint

- **Method:** `GET`
- **Path:** `/columns`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [List columns](https://ru.yougile.com/api-v2#/operations/ColumnController_search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeDeleted` | query | `boolean` | no | Include deleted columns in the result. |
| `title` | query | `string` | no | Filter columns by title. |
| `boardId` | query | `string` | no | Filter columns by board ID. |
