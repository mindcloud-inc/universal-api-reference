# List Inline Comments For Page with Confluence

Retrieves inline comments for a Confluence page.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/pages/:id/inline-comments`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [List Inline Comments For Page](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-comment/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | path | `string` | yes | ID of the Confluence page. |
