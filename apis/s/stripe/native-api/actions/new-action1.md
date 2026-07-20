# List Payouts with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `/payouts?arrival_date[gte]={{arrivalDateGte}}&arrival_date[lte]={{arrivalDateLte}}&status={{status}}&limit={{limit}}`
- **Base URL:** `https://api.stripe.com/v1`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `stripeApiKey` | path | `string` | no |
| `arrivalDateGte` | path | `string` | no |
| `arrivalDateLte` | path | `string` | no |
| `status` | path | `string` | no |
| `limit` | path | `string` | no |
