# List Blog Following with Tumblr

Retrieves blogs followed by a Tumblr blog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/following`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [List Blog Following](https://www.tumblr.com/docs/en/api/v2#following--retrieve-blogs-following)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | The blog whose following list should be retrieved. |
