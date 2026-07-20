# Get Topic Posts with Discourse

Retrieves selected posts from a Discourse topic.

## Endpoint

- **Method:** `GET`
- **Path:** `/t/:id/posts.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Get Topic Posts](https://docs.discourse.org/#tag/Topics/operation/getSpecificPostsFromTopic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Numeric Discourse topic ID. |
