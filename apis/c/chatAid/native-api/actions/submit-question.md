# Submit Question with Chat Aid

Submits a question to Chat Aid for asynchronous completion.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions/custom`
- **Base URL:** `https://api.chataid.com`
- **Official documentation:** [Submit Question](https://docs.chataid.com/api-guide/completion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | The question to answer. |
| `parentTs` | body | `string` | no | Unix timestamp used to maintain conversation context across multiple questions. |
| `messageTs` | body | `string` | no | Unix timestamp of the current message for a follow-up question. |
| `wikiFilters.teams[]` | body | `array<string>` | no | Team IDs to restrict the search scope within the teams accessible to the API key. |
