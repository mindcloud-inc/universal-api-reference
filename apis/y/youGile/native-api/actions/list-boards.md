# List boards with YouGile

Retrieves a list of boards from YouGile.

## Endpoint

- **Method:** `GET`
- **Path:** `/boards`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [List boards](https://ru.yougile.com/api-v2#/operations/BoardController_search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeDeleted` | query | `boolean` | no | Include deleted boards in the result. |
| `title` | query | `string` | no | Filter boards by title. |
| `projectId` | query | `string` | no | Filter boards by project ID. |
