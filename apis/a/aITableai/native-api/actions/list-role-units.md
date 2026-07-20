# List Role Units with AITable.ai

Retrieves units under a role in AITable.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/fusion/v1/spaces/:spaceId/roles/:unitId/units`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [List Role Units](https://developers.aitable.ai/api/reference/#list-units-under-the-role)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID containing the role. |
| `unitId` | path | `string` | yes | AITable role unit ID whose associated units should be listed. |
