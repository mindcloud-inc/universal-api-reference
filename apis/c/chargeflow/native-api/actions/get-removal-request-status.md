# Get Removal Request Status with Chargeflow

Retrieves a data removal request status from Chargeflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/data-subject/removal/{requestId}`
- **Base URL:** `https://api.chargeflow.io/public/2025-04-01`
- **Official documentation:** [Get Removal Request Status](https://docs.chargeflow.io/reference/get_public-2025-04-01-data-subject-removal-requestid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | The Chargeflow removal request ID. |
