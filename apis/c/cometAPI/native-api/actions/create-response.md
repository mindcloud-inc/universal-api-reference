# Create Response with CometAPI

Creates a model response in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/responses`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Create Response](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Input text or structured content for the response. |
| `model` | body | `string` | yes | Responses API model ID. |
