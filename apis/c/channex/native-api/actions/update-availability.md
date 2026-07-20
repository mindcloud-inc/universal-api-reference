# Update Availability with Channex

Updates room type availability in Channex.

## Endpoint

- **Method:** `POST`
- **Path:** `/availability`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Update Availability](https://docs.channex.io/api-v.1-documentation/ari#update-availability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `values[]` | body | `array<object>` | yes | Array of availability update objects documented by Channex. |
