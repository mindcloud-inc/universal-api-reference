# Create Message Batch with CometAPI

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/batches`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Create Message Batch](https://www.cometapi.com/claude-opus-4-5-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requests[]` | body | `array<object>` | yes | Batch requests in Anthropic message format. |
