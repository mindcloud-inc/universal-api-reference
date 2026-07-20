# Update Skill Collection with PromptLayer Run Agent

Updates an existing skill collection in PromptLayer.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/public/v2/skill-collections/:identifier`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Update Skill Collection](https://docs.promptlayer.com/reference/update-skill-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Skill collection UUID, name, or root path. |
| `name` | body | `string` | yes | Updated name for the skill collection. |
