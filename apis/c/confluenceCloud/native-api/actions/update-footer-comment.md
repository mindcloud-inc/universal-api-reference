# Update Footer Comment with Confluence

Updates an existing footer comment in Confluence.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/footer-comments/:commentId`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Update Footer Comment](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-comment/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `commentId` | path | `string` | yes | ID of the footer comment. |
