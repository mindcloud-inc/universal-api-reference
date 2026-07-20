# List Locations with Recruitee ATS

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:company_id/locations`
- **Base URL:** `https://api.recruitee.com`
- **Official documentation:** [List Locations](https://docs.recruitee.com/reference/locations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search query for locations. |
| `scope` | query | `string` | no | Location scope filter. |
| `view_mode` | query | `string` | no | View mode filter. |
