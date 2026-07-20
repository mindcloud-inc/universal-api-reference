# Generate Response with LinkupAPI

Generates an OpenAI-style response through LinkupAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/responses`
- **Base URL:** `https://api.linkup.so/v1`
- **Official documentation:** [Generate Response](https://api.linkup.so/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The prompt or input to generate a response for. |
| `model` | body | `string` | yes | The Linkup model to use for response generation. Accepted values: `0`, `1`. |
| `instructions` | body | `string` | no | Optional system-style instructions for the response. |
| `text` | body | `object` | no | Optional text-format configuration object. |
