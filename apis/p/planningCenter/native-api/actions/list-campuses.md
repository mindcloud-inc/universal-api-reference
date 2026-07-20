# List Campuses with Planning Center

Retrieves campuses from Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/campuses`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List Campuses](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/campus)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Include associated resources |
| `order` | query | `string` | no | Sort returned campuses |
| `where` | query | `object` | no | Equality filters for campus fields |
| `where[created_at]` | query | `date` | no | Query on a specific created_at |
| `where[id]` | query | `number` | no | Query on a specific id |
| `where[updated_at]` | query | `date` | no | Query on a specific updated_at |
