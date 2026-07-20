# Cancel Billing Request with GoCardless

Cancels an existing billing request in GoCardless.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing_requests/:billingRequestId/actions/cancel`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Cancel Billing Request](https://developer.gocardless.com/api-reference/#billing-requests-cancel-a-billing-request)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `billingRequestId` | path | `string` | yes |
| `metadata` | body | `object` | no |
