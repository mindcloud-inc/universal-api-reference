# Update Partner with BoxHero

Updates an existing partner in BoxHero.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/partners/:partner_id`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Update Partner](https://rest.boxhero-app.com/docs/api#/partners/VendorsController_updateVendor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Address of the partner |
| `email` | body | `string` | no | Email address of the partner |
| `memo` | body | `string` | no | Notes for the partner |
| `name` | body | `string` | no | Name of the partner |
| `partner_id` | path | `number` | yes | Unique identifier for the partner |
| `phone` | body | `string` | no | Contact number of the partner |
