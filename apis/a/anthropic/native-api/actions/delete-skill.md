# Delete Skill with Anthropic

Deletes a specific skill from Anthropic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/skills/:skill_id`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Delete Skill](https://platform.claude.com/docs/en/api/beta/skills/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `skill_id` | path | `string` | yes | Identifier of the skill to delete. |
