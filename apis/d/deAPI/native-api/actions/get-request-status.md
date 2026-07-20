# Get Request Status with deAPI

Retrieves the status of an inference job from deAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/client/request-status/:request_id`
- **Base URL:** `https://api.deapi.ai`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | no | The deAPI request identifier to inspect. |
