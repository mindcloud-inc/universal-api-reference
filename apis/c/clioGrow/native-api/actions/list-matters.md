# List Matters with Clio Grow

## Endpoint

- **Method:** `GET`
- **Path:** `/matters`
- **Base URL:** `https://api.clio.com/grow`
- **Official documentation:** [List Matters](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Matters/operation/Matter%23index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_since` | query | `date` | no | Only include matters created on or after this ISO-8601 timestamp. |
| `updated_since` | query | `date` | no | Only include matters updated on or after this ISO-8601 timestamp. |
| `inbox_lead_id` | query | `string` | no | Only include matters associated with this inbox lead ID. |
| `submitted_only` | query | `boolean` | no | Only include submitted matters when true. |
