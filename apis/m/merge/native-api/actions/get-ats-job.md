# Get ATS Job with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ats/v1/jobs/{id}`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [Get ATS Job](https://docs.merge.dev/ats/jobs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
| `id` | path | `string` | yes | Merge object ID. |
