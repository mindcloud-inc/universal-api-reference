# Cancel Loyalty Transaction with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/loyalty/balance/programs/:pid/transactions/:tid/cancel`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Cancel Loyalty Transaction](https://developers.brevo.com/reference/canceltransaction)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pid` | path | `string` | yes |
| `tid` | path | `string` | yes |
