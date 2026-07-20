# List Coauthors For Post with Longreads

Retrieves Longreads coauthors for a specific post.

## Endpoint

- **Method:** `GET`
- **Path:** `/coauthors/v1/coauthors`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [List Coauthors For Post](https://longreads.com/wp-json/coauthors/v1/coauthors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `post_id` | query | `number` | yes | The post ID whose coauthors should be listed. |
