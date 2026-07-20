# Create Post with ChangeCrab

Creates a new post in ChangeCrab.

## Endpoint

- **Method:** `POST`
- **Path:** `/changelogs/:id/posts`
- **Base URL:** `https://changecrab.com/api`
- **Official documentation:** [Create Post](https://changecrab.com/knowledge-base/integrations/api-manage-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ChangeCrab changelog access ID. |
| `summary` | body | `string` | yes | The post title or summary line. |
| `markdown` | body | `string` | yes | The Markdown body for the post. |
| `public` | body | `number` | yes | Use 1 to make the post public. |
| `team` | body | `number` | yes | The owning ChangeCrab team ID. |
