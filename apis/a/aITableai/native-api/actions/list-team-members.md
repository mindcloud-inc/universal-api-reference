# List Team Members with AITable.ai

Retrieves members of a team in AITable.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/fusion/v1/spaces/:spaceId/teams/:unitId/members`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [List Team Members](https://developers.aitable.ai/api/reference/#list-the-team-members)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID containing the team. |
| `unitId` | path | `string` | yes | AITable team unit ID. |
