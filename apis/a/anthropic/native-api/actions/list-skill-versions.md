# List Skill Versions with Anthropic

Retrieves versions for an Anthropic skill.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/skills/:skill_id/versions`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [List Skill Versions](https://platform.claude.com/docs/en/api/beta/skills/versions/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `skill_id` | path | `string` | yes | Identifier of the skill whose versions to list. |
| `limit` | query | `number` | no | Maximum number of versions to return. |
| `page` | query | `string` | no | Opaque page token for pagination. |
