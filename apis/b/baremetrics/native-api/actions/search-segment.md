# Search Segment with Baremetrics

Finds segment results in Baremetrics without saving the segment.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/segments/search`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Search Segment](https://developers.baremetrics.com/reference/search-segment)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sort` | query | `string` | no |
| `order` | query | `string` | no |
| `query[]` | body | `array<object>` | yes |
