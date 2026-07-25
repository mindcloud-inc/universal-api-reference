# Get Balance Transactions with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `/balance_transactions?payout={{payoutId}}&limit={{limit}}&expand[]=data.source&expand[]=data.source.charge`
- **Base URL:** `https://api.stripe.com/v1`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `stripeApiKey` | path | `string` | no |
| `payoutId` | path | `string` | no |
| `limit` | path | `number` | no |
