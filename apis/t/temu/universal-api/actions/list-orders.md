# Temu: List Orders

List orders with optional filters

```
GET https://connect.mindcloud.co/v1/universal/temu/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temu `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/temu/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/temu/latest/actions/list-orders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `regionId` | string | no | Region ID, e.g., USA - 211. |
| `parentOrderLabel` | list<string> | no | List of PO order status labels: - soon_to_be_overdue - past_due - pending_buyer_cancellation - pending_buyer_address_change - pending_risk_control_alert - signature_required_on_delivery Accepts multiple values as an array. |
| `parentOrderStatus` | list<number> | no | Parent order status, default is to query all. 0 :All, 1 :PENDING, Pending status 2 :UN_SHIPPING, Awaiting shipment 3 :CANCELED, Order canceled, 4 :SHIPPED, Order shipped, 5 : RECEIPTED, Order received 41: Partially shipped(only for local mall), 51 :Partially received(only for local mall). |
| `parentOrderSnList` | string | no | List of parent order serial numbers 'parentOrderSn'. **Max 20 per Request** Accepts multiple values as an array. |
| `fulfillmentTypeList` | list<string> | no | Filter by type of order fulfillment. Enum Values: - fulfillBySeller : fulfill by seller, - fulfillByCooperativeWarehouse : fulfill by CooperativeWarehouse. Accepts multiple values as an array. |
| `createdAfter` | date | no | Start time for querying parent order creation, in seconds(timestamp). Defines the starting range of the creation time when querying parent orders. **Must be used in conjunction with createBefore. |
| `createBefore` | date | no | End time for querying parent order creation, in seconds(timestamp). Defines the ending range (closed interval) of the creation time when querying parent orders. **Must be used in conjunction with createAfter. |
| `expectShipLatestTimeStart` | date | no | Start time for querying expected latest shipment, in seconds. |
| `expectShipLatestTimeEnd` | date | no | End time for querying expected latest shipment, in seconds. |
| `updateAtStart` | date | no | Start time for querying order update, in seconds(timestamp). Defines the starting range of the status change time when querying parent orders. **Must be used in conjunction with updateAtEnd. |
| `updateAtEnd` | date | no | End time for querying order update, in seconds(timestamp). Defines the ending range (closed interval) of the status change time when querying parent orders. **Must be used in conjunction with updateAtStart. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchOrderNumberList": {},
      "expectShipLatestTime": "2026-05-07T12:00:00.000Z",
      "fulfillmentWarning": [
        "string"
      ],
      "hasShippingFee": true,
      "latestDeliveryTime": "2026-05-07T12:00:00.000Z",
      "orderList": [
        {
          "canceledQuantityBeforeShipment": 1,
          "earliestTimeBuyShippingLabel": {},
          "earliestTimeGetShippingDocument": {},
          "fulfillmentType": "string",
          "goodsId": 1,
          "goodsName": "Ava Chen",
          "inventoryDeductionWarehouseId": {},
          "inventoryDeductionWarehouseName": {},
          "isCancelledDuringPending": true,
          "orderLabel": [
            {
              "name": "Ava Chen",
              "value": 1
            }
          ],
          "orderPaymentType": "string",
          "orderSn": "string",
          "orderStatus": 1,
          "originalGoodsName": "Ava Chen",
          "originalOrderQuantity": 1,
          "originalSpecName": "Ava Chen",
          "productList": [
            {
              "extCode": "string",
              "productId": 1,
              "productSkuId": 1,
              "soldFactor": 1
            }
          ],
          "quantity": 1,
          "skuId": 1,
          "spec": "string",
          "thumbUrl": "https://example.com"
        }
      ],
      "orderPaymentType": "string",
      "parentOrderLabel": [
        {
          "name": "Ava Chen",
          "value": 1
        }
      ],
      "parentOrderPendingFinishTime": "2026-05-07T12:00:00.000Z",
      "parentOrderSn": "string",
      "parentOrderStatus": 1,
      "parentOrderTime": "2026-05-07T12:00:00.000Z",
      "parentShippingTime": "2026-05-07T12:00:00.000Z",
      "regionId": 1,
      "shippingMethod": 1,
      "siteId": 1,
      "updateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchOrderNumberList` | object |  |
| `expectShipLatestTime` | date |  |
| `fulfillmentWarning[]` | string |  |
| `hasShippingFee` | boolean |  |
| `latestDeliveryTime` | date |  |
| `orderList[].canceledQuantityBeforeShipment` | number |  |
| `orderList[].earliestTimeBuyShippingLabel` | object |  |
| `orderList[].earliestTimeGetShippingDocument` | object |  |
| `orderList[].fulfillmentType` | string |  |
| `orderList[].goodsId` | number |  |
| `orderList[].goodsName` | string |  |
| `orderList[].inventoryDeductionWarehouseId` | object |  |
| `orderList[].inventoryDeductionWarehouseName` | object |  |
| `orderList[].isCancelledDuringPending` | boolean |  |
| `orderList[].orderLabel[].name` | string |  |
| `orderList[].orderLabel[].value` | number |  |
| `orderList[].orderPaymentType` | string |  |
| `orderList[].orderSn` | string |  |
| `orderList[].orderStatus` | number |  |
| `orderList[].originalGoodsName` | string |  |
| `orderList[].originalOrderQuantity` | number |  |
| `orderList[].originalSpecName` | string |  |
| `orderList[].productList[].extCode` | string |  |
| `orderList[].productList[].productId` | number |  |
| `orderList[].productList[].productSkuId` | number |  |
| `orderList[].productList[].soldFactor` | number |  |
| `orderList[].quantity` | number |  |
| `orderList[].skuId` | number |  |
| `orderList[].spec` | string |  |
| `orderList[].thumbUrl` | string |  |
| `orderPaymentType` | string |  |
| `parentOrderLabel[].name` | string |  |
| `parentOrderLabel[].value` | number |  |
| `parentOrderPendingFinishTime` | date |  |
| `parentOrderSn` | string |  |
| `parentOrderStatus` | number |  |
| `parentOrderTime` | date |  |
| `parentShippingTime` | date |  |
| `regionId` | number |  |
| `shippingMethod` | number |  |
| `siteId` | number |  |
| `updateTime` | date |  |

## Native endpoint

Through the native Temu API, this operation is `POST /router` (base URL `https://openapi-b-us.temu.com/openapi`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

