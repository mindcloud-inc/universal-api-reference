# List ATS Jobs with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ats/v1/jobs`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [List ATS Jobs](https://docs.merge.dev/ats/jobs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
