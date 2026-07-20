# Update Deal with Freshworks CRM

Updates an existing deal in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `api/deals/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update Deal](https://developers.freshworks.com/crm/api/#update_a_deal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal.contacts_removed_list[]` | body | `array<number>` | no | — |
| `deal.custom_field` | body | `object` | no | — |
| `deal.custom_field.cf_number_of_agents` | body | `number` | no | — |
| `deal.probability` | body | `number` | no | — |
| `id` | path | `number` | no | Unique deal identifier. |
| `deal` | body | `object` | no | Deal fields to update. |
