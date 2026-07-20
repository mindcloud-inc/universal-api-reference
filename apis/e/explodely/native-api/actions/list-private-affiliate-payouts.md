# List Private Affiliate Payouts with Explodely

## Endpoint

- **Method:** `GET`
- **Path:** `/aff`
- **Base URL:** `https://explodely.com/api/v1`
- **Official documentation:** [List Private Affiliate Payouts](https://docs.explodely.com/api/private-affiliate-payouts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affid` | query | `string` | yes | The Explodely affiliate username for the private payout. |
| `productid` | query | `string` | yes | The Explodely product ID or allproducts. |
| `comm` | query | `string` | yes | The private affiliate commission percentage, from 1 to 80. |
