# Create URL Source with DONNAJAMES Easy

Creates a new URL source in DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `chatbot/:uuid/data-source/url`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Create URL Source](https://guide.gpt-trainer.com/api-reference/data-sources/create-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference_source_link` | body | `string` | no | — |
| `uuid` | path | `string` | yes | Chatbot uuid |
| `url` | body | `string` | yes | — |
