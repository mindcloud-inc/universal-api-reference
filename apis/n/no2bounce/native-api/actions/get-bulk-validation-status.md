# Get Bulk Validation Status with no2bounce

Retrieves bulk validation status from no2bounce by tracking ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/n2b_validate_bulk`
- **Base URL:** `https://connect.no2bounce.com/v2`
- **Official documentation:** [Get Bulk Validation Status](https://www.no2bounce.com/api-documentation#validating-api-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingId` | query | `string` | yes | Use the tracking ID returned by Submit Bulk Validation. |
