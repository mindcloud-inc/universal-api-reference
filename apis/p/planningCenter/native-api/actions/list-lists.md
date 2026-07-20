# List Lists with Planning Center

Retrieves lists from Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/lists`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List Lists](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Include associated resources |
| `order` | query | `string` | no | Sort returned lists |
| `where` | query | `object` | no | Equality filters for list fields |
| `where[batch_completed_at]` | query | `date` | no | Query on a specific batch_completed_at |
| `where[created_at]` | query | `date` | no | Query on a specific created_at |
| `where[id]` | query | `number` | no | Query on a specific id |
| `where[name]` | query | `string` | no | Query on a specific name |
| `where[updated_at]` | query | `date` | no | Query on a specific updated_at |
