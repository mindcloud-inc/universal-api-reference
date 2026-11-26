# Create Report Request with Walmart

Use this report to review detailed itemization of Walmart Fulfillment Services (WFS) and Multichannel Solutions (MCS) fees and credits for a selected time period. It provides a transaction-level view of charges, adjustments, and credits to help reconcile final WFS settlements.

## Endpoint

- **Method:** `POST`
- **Path:** `https://marketplace.walmartapis.com/v3/reports/reportRequests`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Create Report Request](https://developer.walmart.com/global-marketplace/reference/getallorders)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dataStartTime` | body | `string` | no |
| `dataEndTime` | body | `string` | no |
| `reportType` | query | `list` | no |
| `reportVersion` | query | `string` | no |
