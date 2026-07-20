# Update Offer Status with Moco

## Endpoint

- **Method:** `PUT`
- **Path:** `/offers/:id/update_status`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Update Offer Status](https://everii-group.github.io/mocoapp-api-docs/sections/offers.html#put-offersidupdate_status)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `status` | body | `string` | no |
