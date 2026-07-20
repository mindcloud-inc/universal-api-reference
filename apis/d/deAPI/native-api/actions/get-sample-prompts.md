# Get Sample Prompts with deAPI

Retrieves sample prompts for AI tasks from deAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/client/prompts/samples`
- **Base URL:** `https://api.deapi.ai`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lang_code` | query | `string` | no | Optional language code for text2speech prompt generation. |
| `topic` | query | `string` | no | Optional topic to guide the generated sample prompt. |
| `type` | query | `string` | no | Sample prompt type such as text2image or text2speech. |
