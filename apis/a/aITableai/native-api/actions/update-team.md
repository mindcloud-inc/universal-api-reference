# Update Team with AITable.ai

Updates an existing team in AITable.ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fusion/v1/spaces/:spaceId/teams/:unitId`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Update Team](https://developers.aitable.ai/api/reference/#update-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID containing the team. |
| `unitId` | path | `string` | yes | AITable team unit ID to update. |
| `name` | body | `string` | yes | Updated team name. |
| `sequence` | body | `number` | no | Optional team ordering sequence. |
