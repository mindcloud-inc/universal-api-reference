# List Settlement Report List with Amazon Seller

Retrieves Settlement reports from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `reports/2021-06-30/reports`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** pageSize / nextToken
- **Official documentation:** [List Settlement Report List](https://developer-docs.amazon.com/sp-api/docs/reports-api-v2021-06-30-reference#getreports)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportTypes` | query | `list` | no | Accepted values: `GET_V2_SETTLEMENT_REPORT_DATA_FLAT_FILE_V2`. |
| `processingStatuses` | query | `list` | no | Send multiple values as a array. |
| `createdSince` | query | `date` | no | — |
| `createdUntil` | query | `date` | no | — |
| `marketplaces` | query | `list` | no | Send multiple values as a array. |
