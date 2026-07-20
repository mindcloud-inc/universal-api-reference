# Create Partner with BoxHero

Creates a new partner in BoxHero.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/partners`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Create Partner](https://rest.boxhero-app.com/docs/api#/partners/VendorsController_createVendor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Address of the partner |
| `email` | body | `string` | no | Email address of the partner |
| `memo` | body | `string` | no | Notes for the partner |
| `name` | body | `string` | no | Name of the partner |
| `phone` | body | `string` | no | Contact number of the partner |
| `type` | body | `number` | yes | Type of partner: 0 supplier, 1 customer |
