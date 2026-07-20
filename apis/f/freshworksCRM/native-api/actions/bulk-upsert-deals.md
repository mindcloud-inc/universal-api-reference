# Bulk Upsert Deals with Freshworks CRM

Finds or creates multiple deals in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/deals/bulk_upsert`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Upsert Deals](https://developers.freshworks.com/crm/api/#bulk_upsert_deal)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `deals[]` | body | `array<object>` | yes |
| `deals[].data` | body | `object` | no |
| `deals[].data.amount` | body | `number` | no |
| `deals[].id` | body | `string` | no |
| `deals[].name` | body | `string` | no |
