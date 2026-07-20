# Create Community Segment with Circle

Creates a new community segment in Circle.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/v2/community_segments`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Create Community Segment](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Community segment title |
| `visible` | body | `boolean` | yes | Segment visibility flag |
| `rules` | body | `object` | yes | Segment rules object |
