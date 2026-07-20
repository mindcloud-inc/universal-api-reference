# Get Tool OpenAPI with Griptape

Retrieves a tool OpenAPI schema from Griptape.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/tools/:tool_id/openapi`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Get Tool OpenAPI](https://docs.griptape.ai/stable/griptape-cloud/tools/run-tool/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tool_id` | path | `string` | yes | The Griptape tool ID whose OpenAPI definition should be retrieved. |
