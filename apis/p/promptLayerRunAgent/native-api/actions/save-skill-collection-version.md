# Save Skill Collection Version with PromptLayer Run Agent

Creates a new PromptLayer skill collection version.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/v2/skill-collections/:identifier/versions`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Save Skill Collection Version](https://docs.promptlayer.com/reference/save-skill-collection-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Skill collection UUID, name, or root path. |
| `file_updates[]` | body | `array<object>` | no | Inline file additions or replacements for the new version. |
| `moves[]` | body | `array<object>` | no | File move operations for the new version. |
| `deletes[]` | body | `array<string>` | no | File paths to delete in the new version. |
| `commit_message` | body | `string` | no | Optional commit message for the saved version. |
| `release_label` | body | `string` | no | Optional release label to assign to the new version. |
