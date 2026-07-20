# Create Basic Post with Circle

Creates a new basic post in Circle.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/v2/posts`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Create Basic Post](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | body | `list<number>` | yes | Space ID for the post |
| `name` | body | `string` | yes | Post title |
| `body` | body | `string` | yes | Post body content |
