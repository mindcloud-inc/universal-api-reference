# Create Segment with Baremetrics

Creates a segment in Baremetrics.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/segments`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Create Segment](https://developers.baremetrics.com/reference/create-segment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query[]` | body | `array<object>` | yes |
| `name` | body | `string` | no |
