# Update Member Tag with Circle

Updates an existing member tag in Circle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/v2/member_tags/[:id]`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Update Member Tag](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Member tag ID |
| `name` | body | `string` | no | Member tag name |
| `display_format` | body | `list` | no | Display format Accepted values: `icon`, `label`. |
