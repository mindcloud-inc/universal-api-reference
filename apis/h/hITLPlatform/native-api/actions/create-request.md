# Create Request with HITL Platform

## Endpoint

- **Method:** `POST`
- **Path:** `/api/loops/:loopId/requests`
- **Base URL:** `https://api.hitl.sh/v1`
- **Official documentation:** [Create Request](https://docs.hitl.sh/api-reference/requests/create-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback_url` | body | `string` | no | Webhook URL to notify when the request completes. |
| `default_response` | body | `string` | no | Fallback response used if the request times out. |
| `image_url` | body | `string` | no | Image URL to review when the content type is image. |
| `loopId` | path | `string` | yes | The loop where the request will be created. |
| `platform` | body | `string` | yes | Source platform creating the request. |
| `priority` | body | `string` | yes | Priority level such as low, medium, high, or critical. |
| `processing_type` | body | `string` | yes | Processing urgency type such as time-sensitive or deferred. |
| `request_text` | body | `string` | yes | Main request content for the reviewer. |
| `response_type` | body | `string` | yes | Expected response type, such as text or single_select. |
| `timeout_seconds` | body | `number` | no | Timeout in seconds for time-sensitive requests. |
| `type` | body | `string` | yes | Content type to review, such as markdown or image. |
