# Update plot with Farmbrite

Updates an existing plot in Farmbrite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/plots/:plot_id`
- **Base URL:** `https://api.farmbrite.com/v1`
- **Official documentation:** [Update plot](https://developers.farmbrite.com/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `plot_id` | path | `string` | yes |
| `description` | body | `string` | no |
