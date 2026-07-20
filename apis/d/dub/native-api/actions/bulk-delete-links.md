# Bulk Delete Links with Dub

Deletes links from Dub in bulk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/links/bulk`
- **Base URL:** `https://api.dub.co`
- **Official documentation:** [Bulk Delete Links](https://dub.co/docs/api-reference/links/bulk-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkIds[]` | query | `array<string>` | yes | Comma-separated list of link IDs to delete. |
