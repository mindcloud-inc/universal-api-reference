# List Roles with AITable.ai

Retrieves roles from a space in AITable.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/fusion/v1/spaces/:spaceId/roles`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [List Roles](https://developers.aitable.ai/api/reference/#list-roles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID whose roles should be listed. |
