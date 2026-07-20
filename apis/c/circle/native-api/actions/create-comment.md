# Create Comment with Circle

Creates a new comment in Circle.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/v2/comments`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Create Comment](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Comment body content |
| `post_id` | body | `list<number>` | yes | Post ID to attach comment to |
