# Create transaction with Farmbrite

Creates a new transaction in Farmbrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions`
- **Base URL:** `https://api.farmbrite.com/v1`
- **Official documentation:** [Create transaction](https://developers.farmbrite.com/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | body | `string` | yes |
| `category` | body | `string` | yes |
| `amount` | body | `number` | yes |
| `date` | body | `date` | yes |
| `description` | body | `string` | no |
