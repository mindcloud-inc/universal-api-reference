# Create Published Doc Subscription with Blaze AI

Creates a published document subscription in Blaze AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspace_id/published_doc_subscriptions`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Create Published Doc Subscription](https://api.blaze.ai/api/documentation#!/subscriptions/postApiV1WWorkspaceIdPublishedDocSubscriptions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `hook_url` | body | `string` | yes |
| `subscription_name` | body | `string` | yes |
