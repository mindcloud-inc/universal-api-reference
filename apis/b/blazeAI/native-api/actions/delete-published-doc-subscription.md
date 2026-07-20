# Delete Published Doc Subscription with Blaze AI

Deletes an existing published document subscription from Blaze AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/w/:workspace_id/published_doc_subscriptions/:id`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Delete Published Doc Subscription](https://api.blaze.ai/api/documentation#!/subscriptions/deleteApiV1WWorkspaceIdPublishedDocSubscriptionsId)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `id` | path | `number` | yes |
