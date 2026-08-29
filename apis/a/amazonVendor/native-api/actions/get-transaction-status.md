# Get Transaction Status with Amazon Vendor

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/directFulfillment/transactions/v1/transactions/:transactionId`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Get Transaction Status](https://developer-docs.amazon.com/sp-api/reference/gettransactionstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionId` | path | `string` | yes | Previously returned in the response to the POST request of a specific transaction. |
