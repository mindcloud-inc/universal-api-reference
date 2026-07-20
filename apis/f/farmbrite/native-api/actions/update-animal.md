# Update animal with Farmbrite

Updates an existing animal in Farmbrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/animals/:animal_id`
- **Base URL:** `https://api.farmbrite.com/v1`
- **Official documentation:** [Update animal](https://developers.farmbrite.com/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `animal_id` | path | `string` | yes |
| `description` | body | `string` | no |
