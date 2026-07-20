# Update Invoice Status with Moco

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:id/update_status`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Update Invoice Status](https://everii-group.github.io/mocoapp-api-docs/sections/invoices.html#put-invoicesidupdate_status)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `status` | body | `string` | no |
