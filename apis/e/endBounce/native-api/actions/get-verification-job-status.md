# Get Verification Job Status with EndBounce

Retrieves a verification job status from EndBounce.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/jobs/:request_id/status`
- **Base URL:** `https://api.endbounce.com/api/integrations`
- **Official documentation:** [Get Verification Job Status](https://app.endbounce.com/integrations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Verification job request ID. |
