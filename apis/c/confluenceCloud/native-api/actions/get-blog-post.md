# Get Blog Post with Confluence

Retrieves a blog post from Confluence.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/blogposts/:id`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Get Blog Post](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-blog-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | path | `string` | yes | ID of the Confluence blog post. |
