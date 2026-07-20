# List Blog Notifications with Tumblr

Retrieves activity notifications for a Tumblr blog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/notifications`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [List Blog Notifications](https://www.tumblr.com/docs/en/api/v2#notifications--retrieve-blogs-activity-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | The blog whose activity feed should be retrieved. |
| `before` | query | `number` | no | Unix epoch timestamp that begins the page. |
| `types` | query | `list<string>` | no | One or more notification types to filter by. Send multiple values as a array. |
| `rollups` | query | `boolean` | no | Whether to roll up similar activity items into single items. |
| `omit_post_ids` | query | `list<string>` | no | One or more of your own post IDs to filter out. Send multiple values as a array. |
