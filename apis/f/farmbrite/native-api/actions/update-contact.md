# Update contact with Farmbrite

Updates an existing contact in Farmbrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contact_id`
- **Base URL:** `https://api.farmbrite.com/v1`
- **Official documentation:** [Update contact](https://developers.farmbrite.com/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_id` | path | `string` | yes |
| `phone` | body | `string` | no |
