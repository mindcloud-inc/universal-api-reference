# Update Community Segment with Circle

Updates an existing community segment in Circle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/v2/community_segments/[:id]`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Update Community Segment](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Community segment ID |
| `title` | body | `string` | no | Segment title |
| `visible` | body | `boolean` | no | Visibility flag |
| `rules` | body | `object` | no | Segment rules object |
