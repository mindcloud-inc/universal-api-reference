# List Deals with Moco

## Endpoint

- **Method:** `GET`
- **Path:** `/deals`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [List Deals](https://everii-group.github.io/mocoapp-api-docs/sections/deals.html#get-deals)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `closed_from` | query | `date` | no |
| `closed_to` | query | `date` | no |
| `company_id` | query | `number` | no |
| `custom_properties` | query | `object` | no |
| `ids` | query | `string` | no |
| `status` | query | `string` | no |
| `tags` | query | `string` | no |
| `updated_after` | query | `date` | no |
