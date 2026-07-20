# List Blog Posts with Confluence

Retrieves a list of blog posts from Confluence.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/blogposts`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [List Blog Posts](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-blog-post/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
