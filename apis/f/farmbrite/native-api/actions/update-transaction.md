# Update transaction with Farmbrite

Updates an existing transaction in Farmbrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/transactions/:transaction_id`
- **Base URL:** `https://api.farmbrite.com/v1`
- **Official documentation:** [Update transaction](https://developers.farmbrite.com/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `transaction_id` | path | `string` | yes |
| `description` | body | `string` | no |
