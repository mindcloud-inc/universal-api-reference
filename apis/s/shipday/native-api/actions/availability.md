# Availability with Shipday

Checks on-demand service availability in Shipday.

## Endpoint

- **Method:** `POST`
- **Path:** `/on-demand/availability`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Availability](https://docs.shipday.com/reference/availability-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pickupAddress` | body | `string` | yes | Pickup address used for on-demand availability lookup. |
| `deliveryAddress` | body | `string` | yes | Delivery address used for on-demand availability lookup. |
| `deliveryTime` | body | `date` | yes | Requested delivery timestamp for the availability check. |
