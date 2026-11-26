# Check Settlement Report Request Status with Walmart

Status values: RECEIVED, INPROGRESS, READY, ERROR.

## Endpoint

- **Method:** `GET`
- **Path:** `https://marketplace.walmartapis.com/v3/reports/reportRequests/:requestId`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Check Settlement Report Request Status](https://developer.walmart.com/global-marketplace/reference/getallorders)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `requestId` | path | `string` | no |
