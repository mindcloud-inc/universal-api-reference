# Update Page Title with Confluence

Updates an existing page title in Confluence.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/pages/:id/title`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Update Page Title](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | path | `string` | yes | ID of the Confluence page. |
| `title` | body | `string` | yes | New title for the page. |
| `version.number` | body | `number` | yes | Incremented page version required when updating a page title. |
| `status` | body | `string` | yes | Current page status required by Confluence when updating a page title, usually current. |
