# Moderate Input with Open AI

Moderates text or image inputs in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/moderations`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Moderate Input](https://developers.openai.com/api/reference/resources/moderations/methods/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Input text to moderate. |
| `model` | body | `list` | no | Moderation model ID. |
