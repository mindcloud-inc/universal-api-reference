# List Sub Teams with AITable.ai

Retrieves sub teams from AITable.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/fusion/v1/spaces/:spaceId/teams/:unitId/children`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [List Sub Teams](https://developers.aitable.ai/api/reference/#list-sub-teams)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID containing the parent team. |
| `unitId` | path | `string` | yes | AITable parent team unit ID. |
