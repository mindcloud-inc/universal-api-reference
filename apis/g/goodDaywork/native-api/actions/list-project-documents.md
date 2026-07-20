# List Project Documents with GoodDay.work

Finds documents in a GoodDay.work project.

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:projectId/documents`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [List Project Documents](https://www.goodday.work/developers/api-v2/documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | GoodDay project ID. |
| `subfolders` | query | `boolean` | no | Include documents from nested folders. |
