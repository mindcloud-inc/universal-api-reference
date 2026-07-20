# Cancel Payment with GoCardless

Cancels an existing payment in GoCardless.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/:identity/actions/cancel`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Cancel Payment](https://developer.gocardless.com/api-reference/#payments-cancel-a-payment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `identity` | path | `string` | yes |
| `metadata` | body | `object` | no |
