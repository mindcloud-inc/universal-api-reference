# Get Billing Request with GoCardless

Retrieves a single billing request from GoCardless.

## Endpoint

- **Method:** `GET`
- **Path:** `/billing_requests/:billingRequestId`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Get Billing Request](https://developer.gocardless.com/api-reference/#billing-requests-get-a-single-billing-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billingRequestId` | path | `string` | yes | ID of the billing request to fetch. |
