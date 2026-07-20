# Create Depot with Detrack

Creates a new depot in Detrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/dn/depots`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Create Depot](https://detrackapiv2.docs.apiary.io/#reference/depots/create-depot-bulk-update-delete-depots/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.name` | body | `string` | yes | Depot name. |
| `data.address` | body | `string` | yes | Depot address that can be geocoded. |
