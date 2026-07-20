# List Blog Blocks with Tumblr

Retrieves blocked blogs for a Tumblr blog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/blocks`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [List Blog Blocks](https://www.tumblr.com/docs/en/api/v2#blocks--retrieve-blogs-blocks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | The blog whose blocks should be retrieved. |
