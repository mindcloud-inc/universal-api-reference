# Generate Related Skills with SharpAPI

Creates a related skills job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr/related_skills`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Generate Related Skills](https://sharpapi.com/en/catalog/ai/hr-tech/related-skills-generator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Skill to generate related skills for. |
| `language` | body | `string` | no | Language for the related skills output. |
| `max_quantity` | body | `number` | no | Maximum number of related skills to generate. |
