# List Purchases with Moco

## Endpoint

- **Method:** `GET`
- **Path:** `/purchases`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [List Purchases](https://everii-group.github.io/mocoapp-api-docs/sections/purchases.html#get-purchases)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `category_id` | query | `number` | no |
| `company_id` | query | `number` | no |
| `custom_properties` | query | `object` | no |
| `date` | query | `string` | no |
| `identifier` | query | `string` | no |
| `ids` | query | `string` | no |
| `not_booked` | query | `boolean` | no |
| `payment_method` | query | `string` | no |
| `receipt_identifier` | query | `string` | no |
| `status` | query | `string` | no |
| `tags` | query | `string` | no |
| `term` | query | `string` | no |
| `unpaid` | query | `boolean` | no |
| `updated_after` | query | `date` | no |
