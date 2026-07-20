# Update Community Member with Circle

Updates an existing community member in Circle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/v2/community_members/[:id]`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Update Community Member](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Community member ID |
| `name` | body | `string` | no | Community member name |
| `headline` | body | `string` | no | Community member headline |
| `is_flagged` | body | `boolean` | no | Flag member state |
| `member_tag_ids[]` | body | `array<number>` | no | Member tag IDs |
| `space_ids[]` | body | `array<number>` | no | Space IDs |
| `space_group_ids[]` | body | `array<number>` | no | Space group IDs |
