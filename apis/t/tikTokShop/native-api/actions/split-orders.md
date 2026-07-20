# Split Orders with TikTok Shop

Use this API to confirm an order split. Note that ​​supported split levels vary by region​​:
- Some regions support ​​item-level splits​​ (splitting individual units of the same SKU).
- Others only support ​​all-units splits​​ (splitting different SKUs into separate packages).

Here are two examples of supported splits:
- ​​Case 1: all-units split​​, applicable for orders in BR, SEA, MX (local sellers)
Split a buyer order of SKU A of quantity 2 and SKU B of quantity 1 into two separate packages:
  - ​​Package 1​​: all units of SKU A
​​  - Package 2​​: all units of SKU B

- ​​Case 2: item-level split​​, applicable for orders in EU, JP, MX (global sellers), UK, US
Split the same order contents into three individual packages:
  - ​​Package 1​​: 1 unit of SKU A
​  - ​Package 2​​: 1 unit of SKU A
​​  - Package 3​​: 1 unit of SKU B

## Endpoint

- **Method:** `POST`
- **Path:** `fulfillment/202309/orders/:order_id/split`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Split Orders](https://partner.tiktokshop.com/docv2/page/split-orders-202309)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `splittableGroups` | body | `object` | no | Input list of splittable groups. |
| `splittableGroups.id` | body | `string` | no | A unique identifier designated by the developer. This identifier will represent a group of items that will be split into a new package. Once split is confirmed, the platform will be assigned a new package ID for this group of items.  For example, if you input 123 as request, the response will return 123 as your unique identification. The seller uses this field to label each group of items that have been split, and the platform will assign new package IDs to them. |
| `orderId` | path | `string` | no | — |
| `splittableGroups.orderLineitemids[]` | body | `array` | no | The order line item IDs that need to be split into this group. |
