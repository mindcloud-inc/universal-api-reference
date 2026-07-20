# Get Skill Collection with PromptLayer Run Agent

Retrieves a PromptLayer skill collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/v2/skill-collections/:identifier`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Get Skill Collection](https://docs.promptlayer.com/reference/get-skill-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Skill collection UUID, name, or root path. |
| `format` | query | `list` | no | Optional response format. Use zip for an archive download. |
| `label` | query | `string` | no | Release label for the version to fetch. |
| `version` | query | `number` | no | Specific version number to fetch. |
