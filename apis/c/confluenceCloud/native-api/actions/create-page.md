# Create Page with Confluence

Creates a new page in Confluence.

## Endpoint

- **Method:** `POST`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/pages`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Create Page](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
