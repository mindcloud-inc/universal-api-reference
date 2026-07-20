# Update Post with ChangeCrab

Updates an existing post in ChangeCrab.

## Endpoint

- **Method:** `PUT`
- **Path:** `/changelogs/:id/posts/:postId`
- **Base URL:** `https://changecrab.com/api`
- **Official documentation:** [Update Post](https://changecrab.com/knowledge-base/integrations/api-manage-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ChangeCrab changelog access ID. |
| `postId` | path | `number` | yes | The ChangeCrab post ID. |
| `summary` | body | `string` | yes | The post title or summary line. |
| `markdown` | body | `string` | yes | The Markdown body for the post. |
| `public` | body | `number` | yes | Use 1 to make the post public. |
| `team` | body | `number` | yes | The owning ChangeCrab team ID. |
