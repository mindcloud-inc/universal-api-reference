# Update Access Group with Circle

Updates an existing access group in Circle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/v2/access_groups/[:id]`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Update Access Group](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Access group ID |
| `access_group` | body | `object` | yes | Access group update payload |
