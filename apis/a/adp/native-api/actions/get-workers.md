# List Workers with ADP

Request the list of all available workers.

## Endpoint

- **Method:** `GET`
- **Path:** `hr/v2/workers`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [List Workers](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-hr-workers-v2-workers?operation=GET%2Fhr%2Fv2%2Fworkers#swagger)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json;masked=false` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | **Example:** - workers/workAssignments/positionID eq 'MR2000056' |
| `changedSince` | query | `string` | no | — |
| `expand` | query | `string` | no | — |
