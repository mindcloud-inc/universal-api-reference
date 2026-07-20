# Query Draft Items with Plasmic

Retrieves draft items from Plasmic CMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/{cmsId}/tables/:modelId/query`
- **Base URL:** `https://data.plasmic.app/api/v1/cms`
- **Official documentation:** [Query Draft Items](https://docs.plasmic.app/learn/plasmic-cms-api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | The Plasmic CMS model identifier to query in draft mode. |
| `q` | query | `string` | no | A JSON-encoded Plasmic query object used to constrain draft rows. |
| `locale` | query | `string` | no | Optional locale tag such as ar-JO. |
