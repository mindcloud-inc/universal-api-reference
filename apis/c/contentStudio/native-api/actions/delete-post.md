# Delete Post with ContentStudio

Deletes a social media post from ContentStudio, optionally deleting it from platforms.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workspaces/:workspace_id/posts/:post_id`
- **Base URL:** `https://api.contentstudio.io/api/v1`
- **Official documentation:** [Delete Post](https://api-prod.contentstudio.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_ids[]` | body | `array<string>` | no | Specific platform account IDs to target. |
| `delete_from_social` | body | `boolean` | no | Delete from social platforms before removing from ContentStudio. |
| `post_id` | path | `string` | yes | ContentStudio post ID. |
| `workspace_id` | path | `string` | yes | ContentStudio workspace ID. |
