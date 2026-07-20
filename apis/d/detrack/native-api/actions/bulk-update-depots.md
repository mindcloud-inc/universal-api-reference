# Bulk Update Depots with Detrack

Updates multiple depots in Detrack at once.

## Endpoint

- **Method:** `PUT`
- **Path:** `/dn/depots`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Bulk Update Depots](https://detrackapiv2.docs.apiary.io/#reference/depots/create-depot-bulk-update-delete-depots/bulk-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of depot update objects with name and nested data fields. |
