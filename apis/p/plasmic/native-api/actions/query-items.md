# Query Items with Plasmic

Retrieves items from Plasmic CMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/{cmsId}/tables/:modelId/query`
- **Base URL:** `https://data.plasmic.app/api/v1/cms`
- **Official documentation:** [Query Items](https://docs.plasmic.app/learn/plasmic-cms-api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | The Plasmic CMS model identifier to query. |
| `q` | query | `string` | no | A JSON-encoded Plasmic query object, for example {"where":{"slug":"my-item"},"limit":1}. |
| `locale` | query | `string` | no | Optional locale tag such as ar-JO. |
