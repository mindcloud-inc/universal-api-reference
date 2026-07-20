# Add Invoice Payment with Outseta

Creates an invoice payment in Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing/transactions/payment`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Add Invoice Payment](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Account.Uid` | body | `string` | no |
| `Invoice.Uid` | body | `string` | no |
| `Amount` | body | `number` | no |
