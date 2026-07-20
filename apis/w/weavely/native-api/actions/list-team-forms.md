# List Team Forms with Weavely

Retrieves forms from a Weavely team.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:teamId/forms`
- **Base URL:** `https://api.weavely.ai/v1`
- **Official documentation:** [List Team Forms](https://help.weavely.ai/developers/identity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | The unique identifier of the team. |
| `published` | query | `boolean` | no | If true, only returns forms that have a published version. |
