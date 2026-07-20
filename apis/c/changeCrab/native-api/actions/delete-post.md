# Delete Post with ChangeCrab

Deletes an existing post from ChangeCrab.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/changelogs/:id/posts/:postId`
- **Base URL:** `https://changecrab.com/api`
- **Official documentation:** [Delete Post](https://changecrab.com/knowledge-base/integrations/api-manage-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ChangeCrab changelog access ID. |
| `postId` | path | `number` | yes | The ChangeCrab post ID. |
