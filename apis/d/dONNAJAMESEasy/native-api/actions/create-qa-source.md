# Create QA Source with DONNAJAMES Easy

Creates a new QA source in DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `chatbot/:uuid/data-source/qa`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Create QA Source](https://guide.gpt-trainer.com/api-reference/data-sources/create-qa)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference_source_link` | body | `string` | no | — |
| `uuid` | path | `string` | yes | Chatbot uuid |
| `question` | body | `string` | yes | — |
| `answer` | body | `string` | yes | — |
