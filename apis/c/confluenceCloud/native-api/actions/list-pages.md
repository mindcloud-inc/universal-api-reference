# List Pages with Confluence

Retrieves a list of pages from Confluence.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/pages`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [List Pages](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
