# Bulk Create Depots with Detrack

Creates multiple depots in Detrack at once.

## Endpoint

- **Method:** `POST`
- **Path:** `/dn/depots/bulk`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Bulk Create Depots](https://detrackapiv2.docs.apiary.io/#reference/depots/bulk-create-depots/bulk-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of depot objects with name and address. |
