# Create AI Prompt Template with NEXT

Creates a new AI prompt template in NEXT.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai-prompt-templates`
- **Base URL:** `https://rest.eu-west-1.nextapp.co/v1`
- **Official documentation:** [Create AI Prompt Template](https://developer.nextapp.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The prompt template name. |
| `prompt` | body | `string` | yes | The prompt instructions. |
| `suitable` | body | `string` | yes | Which highlight scope this prompt template is suitable for. |
