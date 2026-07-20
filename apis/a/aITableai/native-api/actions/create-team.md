# Create Team with AITable.ai

Creates a new team in AITable.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/fusion/v1/spaces/:spaceId/teams`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Create Team](https://developers.aitable.ai/api/reference/#create-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID where the team will be created. |
| `name` | body | `string` | yes | Name of the team to create. |
| `parentUnitId` | body | `string` | no | Optional parent team unit ID. |
