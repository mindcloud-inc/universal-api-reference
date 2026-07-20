# Get Member with AITable.ai

Retrieves a member from a space in AITable.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/fusion/v1/spaces/:spaceId/members/:unitId`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Get Member](https://developers.aitable.ai/api/reference/#get-a-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID containing the member. |
| `unitId` | path | `string` | yes | AITable member unit ID. |
