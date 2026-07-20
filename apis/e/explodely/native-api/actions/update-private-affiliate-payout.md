# Update Private Affiliate Payout with Explodely

Updates a private affiliate payout in Explodely.

## Endpoint

- **Method:** `POST`
- **Path:** `/aff`
- **Base URL:** `https://explodely.com/api/v1`
- **Official documentation:** [Update Private Affiliate Payout](https://docs.explodely.com/api/edit-private-affiliate-payout)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affid` | body | `string` | yes | The Explodely affiliate username for the private payout. |
| `productid` | body | `string` | yes | The Explodely product ID or allproducts. |
| `comm` | body | `string` | yes | The private affiliate commission percentage, from 1 to 80. |
