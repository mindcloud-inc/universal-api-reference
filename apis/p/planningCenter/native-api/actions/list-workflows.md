# List Workflows with Planning Center

Retrieves workflows from Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/workflows`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List Workflows](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/workflow)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Include associated resources |
| `order` | query | `string` | no | Sort returned workflows |
| `where` | query | `object` | no | Equality filters for workflow fields |
| `where[archived_at]` | query | `date` | no | Query on a specific archived_at |
| `where[campus_id]` | query | `number` | no | Query on a specific campus_id |
| `where[created_at]` | query | `date` | no | Query on a specific created_at |
| `where[deleted_at]` | query | `date` | no | Query on a specific deleted_at |
| `where[id]` | query | `number` | no | Query on a specific id |
| `where[name]` | query | `string` | no | Query on a specific name |
| `where[updated_at]` | query | `date` | no | Query on a specific updated_at |
| `where[workflow_category_id]` | query | `number` | no | Query on a specific workflow_category_id |
