# Check Prompt Safety with ModelsLab

Checks a prompt for safety issues in ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/check_nsfw_cp`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Check Prompt Safety](https://docs.modelslab.com/general-api/nsfw-prompt-check)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | no | Prompt text to check for NSFW or CP content. |
