# Create contact with Farmbrite

Creates a new contact in Farmbrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.farmbrite.com/v1`
- **Official documentation:** [Create contact](https://developers.farmbrite.com/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `first_name` | body | `string` | yes |
| `last_name` | body | `string` | yes |
| `email` | body | `string` | yes |
