# Publish Prompt Template with PromptLayer Run Agent

Publishes a prompt template in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/prompt-templates`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Publish Prompt Template](https://docs.promptlayer.com/reference/templates-publish)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt_template` | body | `object` | yes | Template registry metadata including prompt_name, tags, and optional folder_id. |
| `prompt_version` | body | `object` | yes | Prompt version payload including prompt_template content and commit_message. |
| `release_labels[]` | body | `array<string>` | no | Optional release labels to assign to the published version. |
