# Compact Response with Open AI

Compacts a response in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/responses/compact`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Compact Response](https://developers.openai.com/api/reference/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<object>` | yes | Conversation input to compact. |
| `model` | body | `string` | yes | Model ID used for compaction. |
