# Create Message Batch with Anthropic

Creates a new message batch in Anthropic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/batches`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Create Message Batch](https://platform.claude.com/docs/en/api/messages/batches/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requests[]` | body | `array<object>` | yes | List of requests to process in the batch. |
