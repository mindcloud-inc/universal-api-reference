# Create Stream with Faraday

Finds a stream in Faraday, or creates one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/streams/:stream_name`
- **Base URL:** `https://api.faraday.ai/v1`
- **Official documentation:** [Create Stream](https://faraday.ai/docs/reference/findorcreatestream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stream_name` | path | `string` | no | Faraday stream name. |
