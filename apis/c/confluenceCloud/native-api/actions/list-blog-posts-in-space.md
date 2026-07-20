# List Blog Posts In Space with Confluence

Retrieves blog posts from a Confluence space.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/spaces/:id/blogposts`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [List Blog Posts In Space](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-space/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | path | `string` | yes | ID of the Confluence space. |
