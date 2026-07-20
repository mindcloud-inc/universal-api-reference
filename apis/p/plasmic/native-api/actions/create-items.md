# Create Items with Plasmic

Creates items in Plasmic CMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{cmsId}/tables/:modelId/rows`
- **Base URL:** `https://data.plasmic.app/api/v1/cms`
- **Official documentation:** [Create Items](https://docs.plasmic.app/learn/plasmic-cms-api-reference/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `content-type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | The Plasmic CMS model identifier to create rows in. |
| `rows[]` | body | `array<object>` | yes | An array of row payloads to create, wrapped as { rows: [...] }. |
| `publish` | query | `string` | no | Pass 1 to automatically publish the created rows. |
