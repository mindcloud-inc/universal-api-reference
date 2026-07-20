# Add Affiliate To Affiliate Referral Contract with Explodely

Updates an affiliate referral contract in Explodely by adding an affiliate.

## Endpoint

- **Method:** `POST`
- **Path:** `/aff`
- **Base URL:** `https://explodely.com/api/v1`
- **Official documentation:** [Add Affiliate To Affiliate Referral Contract](https://docs.explodely.com/api/add-affiliate-to-affiliate-referral-contract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractid` | body | `string` | yes | The affiliate referral contract ID. |
| `affid` | body | `string` | yes | The Explodely affiliate username to add to the contract. |
