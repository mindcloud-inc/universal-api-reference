# Initialise Billing Request Flow with GoCardless

Initialises a GoCardless billing request flow.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing_request_flows/:billingRequestFlowId/actions/initialise`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Initialise Billing Request Flow](https://developer.gocardless.com/api-reference/#billing-request-flows-initialise-a-billing-request-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billingRequestFlowId` | path | `string` | yes | ID of the billing request flow to initialise. |
