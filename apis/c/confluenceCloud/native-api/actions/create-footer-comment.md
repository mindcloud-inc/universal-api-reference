# Create Footer Comment with Confluence

Creates a new footer comment in Confluence.

## Endpoint

- **Method:** `POST`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/footer-comments`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Create Footer Comment](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-comment/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
