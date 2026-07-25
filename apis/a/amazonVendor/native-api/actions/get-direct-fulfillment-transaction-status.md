# Get Direct Fulfillment Transaction Status with Amazon Vendor

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/directFulfillment/transactions/2021-12-28/transactions/:transactionId`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Get Direct Fulfillment Transaction Status](https://developer-docs.amazon.com/sp-api/reference/gettransactionstatus-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionId` | path | `string` | yes | Transaction identifier returned from a Direct Fulfillment POST request. |
