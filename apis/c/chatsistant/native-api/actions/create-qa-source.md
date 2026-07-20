# Create QA Source with Chatsistant

Creates a new QA source in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/data-source/qa`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Create QA Source](https://docs.chatsistant.com/api-reference/data-sources/create-qa)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `answer` | body | `string` | no | The answer text. |
| `question` | body | `string` | no | The question text. |
| `uuid` | path | `string` | no | The chatbot UUID. |
