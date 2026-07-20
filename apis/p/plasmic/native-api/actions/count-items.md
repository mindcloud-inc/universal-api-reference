# Count Items with Plasmic

Counts items in Plasmic CMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/{cmsId}/tables/:modelId/count`
- **Base URL:** `https://data.plasmic.app/api/v1/cms`
- **Official documentation:** [Count Items](https://docs.plasmic.app/learn/plasmic-cms-api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | The Plasmic CMS model identifier to count. |
| `q` | query | `string` | no | A JSON-encoded Plasmic query object used to constrain the count. |
| `locale` | query | `string` | no | Optional locale tag such as ar-JO. |
