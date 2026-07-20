# Initialize Quantities with Synchroteam

Initializes part quantities in Synchroteam stock depots.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Api/v2/Inventory/Quantities`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Initialize Quantities](https://api.synchroteam.com/v2/#initialize-the-quantities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `object` | yes | Request body payload for updating inventory quantities (per docs). |
