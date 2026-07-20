# Retry Payment with GoCardless

Retries an existing payment in GoCardless.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/:identity/actions/retry`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Retry Payment](https://developer.gocardless.com/api-reference/#payments-retry-a-payment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `identity` | path | `string` | yes |
| `charge_date` | body | `date` | no |
| `metadata` | body | `object` | no |
