# Get Space with Confluence

Retrieves an existing space from Confluence.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/spaces/:id`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Get Space](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-space/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | path | `string` | yes | ID of the Confluence space. |
