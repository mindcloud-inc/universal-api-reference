# List Transactions with Amazon Seller

Retrieves finance transactions from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `finances/2024-06-19/transactions`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [List Transactions](https://developer-docs.amazon.com/sp-api/reference/listtransactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postedAfter` | query | `date` | no | Include transactions posted on or after this ISO 8601 date-time. This must be more than two minutes before the request time. |
| `postedBefore` | query | `date` | no | Include transactions posted before this ISO 8601 date-time. It must be later than Posted After and defaults to two minutes before the request time. |
| `marketplaceId` | query | `string` | no | Filter transactions to a specific marketplace ID. |
| `transactionStatus` | query | `string` | no | Filter by transaction status: DEFERRED, RELEASED, or DEFERRED_RELEASED. |
| `relatedIdentifierName` | query | `string` | no | Filter by identifier type: FINANCIAL_EVENT_GROUP_ID or ORDER_ID. |
| `relatedIdentifierValue` | query | `string` | no | — |
