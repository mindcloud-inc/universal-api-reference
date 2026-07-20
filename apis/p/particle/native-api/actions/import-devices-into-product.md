# Import Devices into Product with Particle

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/products/:productIdOrSlug/devices`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Import Devices into Product](https://docs.particle.io/reference/cloud-apis/api/#import-devices-into-product)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | yes |
| `productIdOrSlug` | path | `string` | yes |
