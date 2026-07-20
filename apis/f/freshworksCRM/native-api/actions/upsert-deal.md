# Upsert Deal with Freshworks CRM

Finds a deal in Freshworks CRM, or creates one if no match is found.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/deals/upsert`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Upsert Deal](https://developers.freshworks.com/crm/api/#upsert_a_deal)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `deal` | body | `object` | yes |
| `deal.amount` | body | `number` | no |
| `unique_identifier` | body | `object` | yes |
| `unique_identifier.id` | body | `string` | yes |
