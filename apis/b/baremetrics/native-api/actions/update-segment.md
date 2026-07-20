# Update Segment with Baremetrics

Updates a segment in Baremetrics.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/segments/:id`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Update Segment](https://developers.baremetrics.com/reference/update-segment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `query[]` | body | `array<object>` | no |
