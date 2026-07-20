# Add Unscheduled Orders Bulk with Track-POD

Creates new unscheduled orders in bulk in Track-POD.

## Endpoint

- **Method:** `POST`
- **Path:** `/Order/Bulk`
- **Base URL:** `https://api.track-pod.com`
- **Official documentation:** [Add Unscheduled Orders Bulk](https://api.track-pod.com/index.html#/Order/AddOrderBulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Orders[0].Address` | body | `string` | no | First bulk order address. |
| `Orders[0].Client` | body | `string` | no | First bulk order client name. |
| `Orders[0].ContactName` | body | `string` | no | First bulk order contact name. |
| `Orders[0].Date` | body | `string` | no | First bulk order date and time. |
| `Orders[0].Number` | body | `string` | no | First bulk order number. |
| `Orders[0].Phone` | body | `string` | no | First bulk order phone number. |
| `Orders[0].TimeSlotFrom` | body | `string` | no | First bulk order time window start. |
| `Orders[0].TimeSlotTo` | body | `string` | no | First bulk order time window end. |
| `Orders[1].Address` | body | `string` | no | Second bulk order address. |
| `Orders[1].Client` | body | `string` | no | Second bulk order client name. |
| `Orders[1].ContactName` | body | `string` | no | Second bulk order contact name. |
| `Orders[1].Date` | body | `string` | no | Second bulk order date and time. |
| `Orders[1].Number` | body | `string` | no | Second bulk order number. |
| `Orders[1].Phone` | body | `string` | no | Second bulk order phone number. |
| `Orders[1].TimeSlotFrom` | body | `string` | no | Second bulk order time window start. |
| `Orders[1].TimeSlotTo` | body | `string` | no | Second bulk order time window end. |
| `Orders[2].Address` | body | `string` | no | Third bulk order address. |
| `Orders[2].Client` | body | `string` | no | Third bulk order client name. |
| `Orders[2].ContactName` | body | `string` | no | Third bulk order contact name. |
| `Orders[2].Date` | body | `string` | no | Third bulk order date and time. |
| `Orders[2].Number` | body | `string` | no | Third bulk order number. |
| `Orders[2].Phone` | body | `string` | no | Third bulk order phone number. |
| `Orders[2].TimeSlotFrom` | body | `string` | no | Third bulk order time window start. |
| `Orders[2].TimeSlotTo` | body | `string` | no | Third bulk order time window end. |
| `updateAddressGps` | query | `boolean` | no | Force-update existing address latitude/longitude from each payload order. |
| `updateGoodsPrice` | query | `boolean` | no | Force-update existing goods prices from each payload order. |
