# Update Campaign with Tremendous

Updates an existing campaign in Tremendous.

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaigns/:id`
- **Base URL:** `https://testflight.tremendous.com/api/v2`
- **Official documentation:** [Update Campaign](https://developers.tremendous.com/reference/update-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated campaign description |
| `id` | path | `string` | yes | ID of the campaign to update |
| `name` | body | `string` | no | Updated campaign name |
| `products[]` | body | `array<string>` | no | Updated product IDs available in the campaign |
