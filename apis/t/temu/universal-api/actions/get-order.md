# Temu: Get Order

Retrieve detailed information about a specific order.

```
GET https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-order?connectionId=$CONNECTION_ID&parentOrderSn=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parentOrderSn": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-order?${params}`, {
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
| `parentOrderSn` | string | yes | The parent order serial number - 'parentOrderSn' |
| `fulfillmentTypeList` | list<string> | no | The type of order fulfillment Accepts multiple values as an array. |

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
          "packageSnInfo": [
            {
              "callSuccess": true,
              "packageDeliveryType": 1,
              "packageSn": "string"
            }
          ],
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
      "regionName1": "Ava Chen",
      "regionName2": "Ava Chen",
      "regionName3": "Ava Chen",
      "shippingMethod": 1,
      "siteId": 1
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
| `orderList[].packageSnInfo[].callSuccess` | boolean |  |
| `orderList[].packageSnInfo[].packageDeliveryType` | number |  |
| `orderList[].packageSnInfo[].packageSn` | string |  |
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
| `regionName1` | string |  |
| `regionName2` | string |  |
| `regionName3` | string |  |
| `shippingMethod` | number |  |
| `siteId` | number |  |

## Native endpoint

Through the native Temu API, this operation is `POST /router` (base URL `https://openapi-b-us.temu.com/openapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

