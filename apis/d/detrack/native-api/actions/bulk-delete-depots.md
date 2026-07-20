# Bulk Delete Depots with Detrack

Deletes multiple depots from Detrack at once.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/dn/depots`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Bulk Delete Depots](https://detrackapiv2.docs.apiary.io/#reference/depots/create-depot-bulk-update-delete-depots/bulk-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of depot objects to delete by name. |
