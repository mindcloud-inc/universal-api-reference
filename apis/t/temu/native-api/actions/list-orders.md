# List Orders with Temu

List orders with optional filters

## Endpoint

- **Method:** `POST`
- **Path:** `/router`
- **Base URL:** `https://openapi-b-us.temu.com/openapi`
- **Official documentation:** [List Orders](https://partner-us.temu.com/documentation?menu_code=fb16b05f7a904765aac4af3a24b87d4a&sub_menu_code=554fd46b45ee49269cbdd6d4008a5dc1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `regionId` | body | `string` | no | Region ID, e.g., USA - 211. |
| `parentOrderLabel` | body | `list<string>` | no | List of PO order status labels:  - soon_to_be_overdue - past_due - pending_buyer_cancellation - pending_buyer_address_change - pending_risk_control_alert - signature_required_on_delivery Send multiple values as a array. |
| `parentOrderStatus` | body | `list<number>` | no | Parent order status, default is to query all.  0 :All, 1 :PENDING, Pending status 2 :UN_SHIPPING, Awaiting shipment 3 :CANCELED, Order canceled, 4 :SHIPPED, Order shipped, 5 : RECEIPTED, Order received 41: Partially shipped(only for local mall), 51 :Partially received(only for local mall). |
| `parentOrderSnList` | body | `string` | no | List of parent order serial numbers 'parentOrderSn'.  **Max 20 per Request** Send multiple values as a array. |
| `fulfillmentTypeList` | body | `list<string>` | no | Filter by type of order fulfillment.  Enum Values: - fulfillBySeller : fulfill by seller, - fulfillByCooperativeWarehouse : fulfill by CooperativeWarehouse. Send multiple values as a array. |
| `createdAfter` | body | `date` | no | Start time for querying parent order creation, in seconds(timestamp). Defines the starting range of the creation time when querying parent orders.  **Must be used in conjunction with createBefore. |
| `createBefore` | body | `date` | no | End time for querying parent order creation, in seconds(timestamp). Defines the ending range (closed interval) of the creation time when querying parent orders.  **Must be used in conjunction with createAfter. |
| `expectShipLatestTimeStart` | body | `date` | no | Start time for querying expected latest shipment, in seconds. |
| `expectShipLatestTimeEnd` | body | `date` | no | End time for querying expected latest shipment, in seconds. |
| `updateAtStart` | body | `date` | no | Start time for querying order update, in seconds(timestamp). Defines the starting range of the status change time when querying parent orders.  **Must be used in conjunction with updateAtEnd. |
| `updateAtEnd` | body | `date` | no | End time for querying order update, in seconds(timestamp). Defines the ending range (closed interval) of the status change time when querying parent orders.  **Must be used in conjunction with updateAtStart. |
