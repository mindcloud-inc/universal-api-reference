# List Documents with Doctly

## Endpoint

- **Method:** `GET`
- **Path:** `/documents`
- **Base URL:** `https://api.doctly.ai/api/v1`
- **Official documentation:** [List Documents](https://docs.doctly.ai/api-reference/documents/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extractor_id` | query | `string` | no | Filter by a specific extractor UUID. |
| `no_extractor` | query | `boolean` | no | Return only plain Markdown conversions without an extractor. |
| `search` | query | `string` | no | Case-insensitive partial filename search. |
| `date_from` | query | `string` | no | Filter documents created on or after this ISO 8601 date. |
| `date_to` | query | `string` | no | Filter documents created on or before this ISO 8601 date. |
