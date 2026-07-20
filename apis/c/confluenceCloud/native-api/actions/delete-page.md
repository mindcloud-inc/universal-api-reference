# Delete Page with Confluence

Deletes an existing page from Confluence.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/pages/:id`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Delete Page](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | path | `string` | yes | ID of the Confluence page. |
