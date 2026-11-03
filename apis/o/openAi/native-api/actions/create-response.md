# Create Response with Open AI

Creates a model response in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/responses`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Create Response](https://developers.openai.com/api/reference/resources/responses/methods/create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[].role` | body | `list<string>` | no | — |
| `model` | body | `list<string>` | yes | ID of the model to use for the response (for example, gpt-4.1 or gpt-4o-mini). |
| `reasoning.effort` | body | `list<string>` | no | — |
| `text.format.type` | body | `list<string>` | no | — |
| `input[]` | body | `array<object>` | no | Text, image, or file inputs to the model, used to generate a response. |
| `input[].content[]` | body | `array<object>` | no | — |
| `text.format` | body | `object` | no | — |
| `tools[]` | body | `array<object>` | no | Array of objects listing one for each tool |
| `reasoning` | body | `object` | no | — |
| `text` | body | `object` | no | — |
