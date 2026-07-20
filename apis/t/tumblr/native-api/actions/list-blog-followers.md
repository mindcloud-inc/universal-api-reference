# List Blog Followers with Tumblr

Retrieves followers of a Tumblr blog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/followers`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [List Blog Followers](https://www.tumblr.com/docs/en/api/v2#followers--retrieve-a-blogs-followers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | The blog whose followers should be retrieved. |
