# List Invoices with Moco

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [List Invoices](https://everii-group.github.io/mocoapp-api-docs/sections/invoices.html#get-invoices)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | query | `number` | no |
| `custom_properties` | query | `object` | no |
| `date_from` | query | `date` | no |
| `date_to` | query | `date` | no |
| `identifier` | query | `string` | no |
| `ids` | query | `string` | no |
| `include_disregarded` | query | `boolean` | no |
| `not_booked` | query | `boolean` | no |
| `project_id` | query | `number` | no |
| `service_period_from` | query | `date` | no |
| `service_period_to` | query | `date` | no |
| `status` | query | `string` | no |
| `tags` | query | `string` | no |
| `term` | query | `string` | no |
| `updated_after` | query | `date` | no |
