# Update AI Prompt Template with NEXT

Updates an existing AI prompt template in NEXT.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ai-prompt-templates/:id`
- **Base URL:** `https://rest.eu-west-1.nextapp.co/v1`
- **Official documentation:** [Update AI Prompt Template](https://developer.nextapp.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The AI prompt template ID. |
| `name` | body | `string` | yes | Updated prompt template name. |
| `prompt` | body | `string` | yes | Updated prompt instructions. |
| `suitable` | body | `string` | yes | Updated highlight scope suitability. |
