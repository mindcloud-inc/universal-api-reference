# Create New Response with Grok

Creates a new response in Grok.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/responses`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Create New Response](https://docs.x.ai/developers/rest-api-reference/inference/chat#create-new-response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | no | Model ID to use for the response. |
| `input` | body | `string` | yes | Text or structured input for the response. |
