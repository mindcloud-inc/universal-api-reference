# Bulk Delete Deals with Freshworks CRM

Deletes multiple deals from Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/deals/bulk_destroy`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Delete Deals](https://developers.freshworks.com/crm/api/#bulk_delete_deal)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `selected_ids[]` | body | `array<number>` | yes |
