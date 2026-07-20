# List Transform Jobs with Kazm

Retrieves transform jobs from Kazm.

## Endpoint

- **Method:** `GET`
- **Path:** `/transform-jobs`
- **Base URL:** `https://api.lightningrod.ai/api/public/v1`
- **Official documentation:** [List Transform Jobs](https://docs.lightningrod.ai/rest-api/transform-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor for the next page of transform jobs. |
| `limit` | query | `string` | no | Maximum number of transform jobs to return. |
| `status` | query | `string` | no | Filter transform jobs by status. |
