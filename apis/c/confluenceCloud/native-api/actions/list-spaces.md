# List Spaces with Confluence

Retrieves a list of spaces from Confluence.

## Endpoint

- **Method:** `GET`
- **Path:** `/ex/confluence/:cloudId/wiki/api/v2/spaces`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [List Spaces](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-space/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
