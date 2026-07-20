# List Responses with Refiner

Retrieves survey views and responses from Refiner.

## Endpoint

- **Method:** `GET`
- **Path:** `/responses`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [List Responses](https://refiner.io/docs/api/#get-responses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_uuid` | query | `string` | no | Filter responses for one survey form UUID. |
| `form_uuids[]` | query | `array<string>` | no | Filter responses for multiple survey form UUIDs. |
| `segment_uuid` | query | `string` | no | Filter responses for one segment UUID. |
| `segment_uuids[]` | query | `array<string>` | no | Filter responses for multiple segment UUIDs. |
| `date_range_start` | query | `date` | no | Return responses on or after this ISO 8601 timestamp. |
| `date_range_end` | query | `date` | no | Return responses before this ISO 8601 timestamp. |
| `include` | query | `string` | no | Choose whether to return completed responses only, partials, or all survey views. |
| `search` | query | `string` | no | Match the contact user ID, Refiner UUID, email, or name. |
| `with_attributes` | query | `boolean` | no | Include all stored contact attributes on each response contact. |
| `page_cursor` | query | `string` | no | Cursor for the next response page returned by Refiner. |
