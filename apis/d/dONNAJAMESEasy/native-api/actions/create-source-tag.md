# Create Source Tag with DONNAJAMES Easy

Creates a new source tag in DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `chatbot/:uuid/source-tag/create`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Create Source Tag](https://guide.gpt-trainer.com/api-reference/source-tags/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Chatbot uuid |
| `name` | body | `string` | yes | — |
| `color` | body | `string` | yes | — |
