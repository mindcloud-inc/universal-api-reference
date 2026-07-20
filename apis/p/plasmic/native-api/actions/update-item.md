# Update Item with Plasmic

Updates an item in Plasmic CMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/rows/:rowId`
- **Base URL:** `https://data.plasmic.app/api/v1/cms`
- **Official documentation:** [Update Item](https://docs.plasmic.app/learn/plasmic-cms-api-reference/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `content-type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rowId` | path | `string` | yes | The Plasmic row identifier to update. |
| `identifier` | body | `string` | no | Optional row identifier value. |
| `data` | body | `object` | no | Partial row data object. Null clears a field and omitted fields are unchanged. |
| `publish` | query | `string` | no | Pass 1 to automatically publish the updated row. |
