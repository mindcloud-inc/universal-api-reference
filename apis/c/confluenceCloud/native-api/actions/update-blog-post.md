# Update Blog Post with Confluence

Updates an existing blog post in Confluence.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/blogposts/:id`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Update Blog Post](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-blog-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | path | `string` | yes | ID of the Confluence blog post. |
| `id` | body | `string` | yes | Confluence requires the blog post ID in the request body as well as the path when updating a blog post. |
