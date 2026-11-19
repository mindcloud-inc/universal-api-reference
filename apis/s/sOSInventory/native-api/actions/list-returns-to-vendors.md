# List Returns to Vendors with SOS Inventory

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/returntovendor`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Returns to Vendors](https://developer.sosinventory.com/apidoc/ReturnToVendor)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Match return number, ID, comment, vendor, or location. |
| `status` | query | `list<string>` | no | Accepted values: `closed`, `open`. |
| `archived` | query | `list<string>` | no | Accepted values: `no`, `yes`. |
| `from` | query | `date` | no | — |
| `to` | query | `date` | no | — |
| `location` | query | `list<string>` | no | — |
| `createdsince` | query | `date` | no | — |
| `updatedsince` | query | `date` | no | — |
