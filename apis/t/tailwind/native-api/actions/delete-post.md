# Delete Post with Tailwind

Deletes an existing post from Tailwind.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/accounts/:accountId/posts/:postId`
- **Base URL:** `https://api-v1.tailwind.ai`
- **Official documentation:** [Delete Post](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidpostspostid/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Pinterest account ID. |
| `postId` | path | `string` | yes | Tailwind post ID. |
