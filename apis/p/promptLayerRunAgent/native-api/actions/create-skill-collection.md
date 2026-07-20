# Create Skill Collection with PromptLayer Run Agent

Creates a new skill collection in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/v2/skill-collections`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Create Skill Collection](https://docs.promptlayer.com/reference/create-skill-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the skill collection. |
| `folder_id` | body | `number` | no | Optional folder ID that should contain the skill collection. |
| `provider` | body | `string` | no | Optional provider for the skill collection. |
| `files[]` | body | `array<object>` | yes | Inline files to seed the skill collection. |
| `commit_message` | body | `string` | no | Optional commit message for the initial version. |
