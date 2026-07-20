# Update Topic with Circle

Updates an existing topic in Circle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/v2/topics/[:id]`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Update Topic](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Topic ID |
| `name` | body | `string` | no | Topic name |
| `admin_only` | body | `boolean` | no | Admin only toggle |
| `space_ids[]` | body | `array<number>` | no | Space IDs |
