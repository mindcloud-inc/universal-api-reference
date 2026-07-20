# Update Redemption Status with Absinthe

Updates a redemption's status in Absinthe.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/redemptions/{redemption_id}`
- **Base URL:** `https://api.absinthe.network`
- **Official documentation:** [Update Redemption Status](https://api.absinthe.network/doc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `redemption_id` | path | `string` | no |
| `status` | body | `string` | no |
