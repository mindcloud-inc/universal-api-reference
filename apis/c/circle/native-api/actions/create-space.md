# Create Space with Circle

Creates a new space in Circle.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/v2/spaces`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Create Space](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_group_id` | body | `number` | yes | Space group ID |
| `name` | body | `string` | yes | Space name |
| `slug` | body | `string` | yes | Space slug |
