# Update Basic Post with Circle

Updates an existing basic post in Circle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/v2/posts/[:id]`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Update Basic Post](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Post ID |
| `name` | body | `string` | no | Post name |
| `tiptap_body` | body | `object` | no | Tiptap body payload |
