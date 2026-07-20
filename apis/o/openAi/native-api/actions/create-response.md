# Create Response with Open AI

Creates a model response in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/responses`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Create Response](https://developers.openai.com/api/reference/resources/responses/methods/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<object>` | no | Text, image, or file inputs to the model, used to generate a response. |
| `input[].content[].type` | body | `list<string>` | no | — |
| `input[].role` | body | `list<string>` | no | — |
| `text.format.type` | body | `list<string>` | no | — |
| `input[].content[]` | body | `array<object>` | no | — |
| `input[].content[].text` | body | `string` | no | — |
| `model` | body | `list<string>` | yes | ID of the model to use for the response (for example, gpt-4.1 or gpt-4o-mini). |
| `text.format` | body | `object` | no | — |
| `input[].content[].image_url` | body | `string` | no | — |
| `tools[]` | body | `array<object>` | no | Array of objects listing one for each tool |
| `input[].content[].fileUrl` | body | `string` | no | — |
| `text` | body | `object` | no | — |
