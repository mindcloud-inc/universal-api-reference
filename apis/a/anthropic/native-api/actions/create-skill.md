# Create Skill with Anthropic

Creates a new skill in Anthropic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/skills`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Create Skill](https://platform.claude.com/docs/en/api/beta/skills/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `display_title` | body | `string` | no | Optional human-readable title for the skill. |
| `files` | body | `list<string>` | yes | Files to upload as skill inputs (multipart UploadFile fields). |
