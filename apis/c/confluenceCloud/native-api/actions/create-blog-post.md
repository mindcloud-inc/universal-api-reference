# Create Blog Post with Confluence

Creates a new blog post in Confluence.

## Endpoint

- **Method:** `POST`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/blogposts`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Create Blog Post](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-blog-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
