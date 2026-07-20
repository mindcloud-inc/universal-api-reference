# Update Space with Circle

Updates an existing space in Circle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/v2/spaces/[:id]`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Update Space](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Space ID |
| `name` | body | `string` | no | Space name |
| `space_group_id` | body | `number` | no | Space group ID |
