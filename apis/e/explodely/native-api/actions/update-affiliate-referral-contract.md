# Update Affiliate Referral Contract with Explodely

Updates an affiliate referral contract in Explodely.

## Endpoint

- **Method:** `POST`
- **Path:** `/aff`
- **Base URL:** `https://explodely.com/api/v1`
- **Official documentation:** [Update Affiliate Referral Contract](https://docs.explodely.com/api/edit-affiliate-referral-contract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractid` | body | `string` | yes | The affiliate referral contract ID to edit. |
| `affcomm` | body | `string` | yes | The updated partner share percentage, up to 80. |
