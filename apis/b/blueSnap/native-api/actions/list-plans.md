# List Plans with BlueSnap

Retrieves plans from BlueSnap.

## Endpoint

- **Method:** `GET`
- **Path:** `/recurring/plans`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [List Plans](https://developers.bluesnap.com/v8976-JSON/reference/retrieve-all-plans)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Return plans after this plan ID. |
| `before` | query | `string` | no | Return plans before this plan ID. |
| `pagesize` | query | `string` | no | Number of results to return. |
| `status` | query | `string` | no | Filter by plan status. |
| `gettotal` | query | `boolean` | no | Whether to include total results count. |
| `fulldescription` | query | `boolean` | no | Return full plan details. |
