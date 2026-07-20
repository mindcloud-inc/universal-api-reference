# Create Connection Link with InsightIQ

Creates a new connection link in InsightIQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/links`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Connection Link](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | body | `string` | yes | External identifier for the connection link subject. |
| `name` | body | `string` | no | Optional display label for the connection link. |
