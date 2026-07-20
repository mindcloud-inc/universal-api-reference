# List Laboratory Definitions with Cerbo

Retrieves laboratory definitions from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/laboratories`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Laboratory Definitions](https://docs.cer.bo/#tag/Facilities/operation/listFacilities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | query | `string` | no | Returns laboratory listings defined as being in this city. |
| `state` | query | `string` | no | Returns laboratory listings defined as being in this state. |
| `company-brand` | query | `string` | no | Returns laboratory listings of this brand (e.g., "Quest"). |
