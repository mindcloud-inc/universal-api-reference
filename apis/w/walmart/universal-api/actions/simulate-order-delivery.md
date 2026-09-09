# Walmart: Simulate Order Delivery

This request updates an order with delivery information in the Marketplace dynamic sandbox.

```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/simulate-order-delivery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/simulate-order-delivery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaseOrderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/simulate-order-delivery', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "purchaseOrderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderLines.orderLine[]` | array | no |  |
| `orderLines.orderLine[].lineNumber` | number | no | Line number of an item within the order to return. |
| `orderLines.orderLine[].orderLineStatuses.orderLineStatus[]` | array<object> | no |  |
| `orderLines.orderLine[].orderLineStatuses.orderLineStatus[].status` | string | no | Allowed: 'Delivered' Default: `Delivered`. Example: `Delivered`. |
| `purchaseOrderId` | string | yes | Purchase order identifier for the order being used in the return simulation. |
| `orderLines.orderLine[].orderLineStatuses` | object | no | Order line status information. |
| `orderLines` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerEmailId": "ava@example.com",
      "customerName": {
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "customerOrderId": "string",
      "purchaseOrderId": "string",
      "refundMode": "string",
      "replacementCustomerOrderId": "string",
      "returnByDate": "2026-05-07T12:00:00.000Z",
      "returnChannel": {
        "channelName": "Ava Chen"
      },
      "returnLineGroups": [
        {
          "groupNo": 1,
          "returnExpectedFlag": true
        }
      ],
      "returnOrderDate": "2026-05-07T12:00:00.000Z",
      "returnOrderId": "string",
      "returnOrderLines": [
        {
          "cancellableQty": 1,
          "charges": [
            {
              "chargeCategory": "string",
              "chargeName": "Ava Chen",
              "chargePerUnit": {
                "currencyAmount": 1,
                "currencyUnit": "string"
              },
              "excessCharge": {
                "currencyAmount": 1,
                "currencyUnit": "string"
              },
              "isBillable": true,
              "isDiscount": true,
              "references": [
                {
                  "name": "Ava Chen",
                  "value": "string"
                }
              ],
              "tax": [
                {
                  "excessTax": {
                    "currencyAmount": 1,
                    "currencyUnit": "string"
                  },
                  "taxName": "Ava Chen",
                  "taxPerUnit": {
                    "currencyAmount": 1,
                    "currencyUnit": "string"
                  }
                }
              ]
            }
          ],
          "chargeTotals": [
            {
              "name": "Ava Chen",
              "value": {
                "currencyAmount": 1,
                "currencyUnit": "string"
              }
            }
          ],
          "currentDeliveryStatus": "string",
          "currentRefundStatus": "string",
          "currentTrackingStatuses": [
            {
              "currentRefundStatus": "string",
              "quantity": {
                "measurementValue": 1,
                "unitOfMeasure": "string"
              },
              "status": "string",
              "statusTime": "2026-05-07T12:00:00.000Z"
            }
          ],
          "exceptionItemType": "string",
          "isFastReplacement": true,
          "isKeepIt": true,
          "isReturnForException": true,
          "item": {
            "condition": "string",
            "itemWeight": {
              "measurementValue": 1,
              "unitOfMeasure": "string"
            },
            "productName": "Ava Chen",
            "sku": "string"
          },
          "lastItem": true,
          "purchaseOrderId": "string",
          "purchaseOrderLineNumber": 1,
          "quantity": {
            "measurementValue": 1,
            "unitOfMeasure": "string"
          },
          "rechargeableQty": 1,
          "rechargeReason": "string",
          "refundChannels": [
            {
              "quantity": {
                "measurementValue": 1,
                "unitOfMeasure": "string"
              },
              "refundChannelName": "Ava Chen"
            }
          ],
          "refundCoveredBy": "string",
          "refundedQty": 1,
          "returnCancellationReason": "string",
          "returnDescription": "string",
          "returnExpectedFlag": true,
          "returnOrderLineNumber": 1,
          "returnReason": "string",
          "returnTrackingDetail": [
            {
              "eventDescription": "string",
              "eventTag": "string",
              "eventTime": "2026-05-07T12:00:00.000Z",
              "references": [
                {
                  "name": "Ava Chen",
                  "value": "string"
                }
              ],
              "sequenceNo": 1
            }
          ],
          "salesOrderLineNumber": 1,
          "sellerOrderId": "string",
          "status": "string",
          "statusTime": "2026-05-07T12:00:00.000Z",
          "unitPrice": {
            "currencyAmount": 1,
            "currencyUnit": "string"
          }
        }
      ],
      "returnType": "string",
      "totalRefundAmount": {
        "currencyAmount": 1,
        "currencyUnit": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerEmailId` | string |  |
| `customerName.firstName` | string |  |
| `customerName.lastName` | string |  |
| `customerOrderId` | string |  |
| `purchaseOrderId` | string |  |
| `refundMode` | string |  |
| `replacementCustomerOrderId` | string |  |
| `returnByDate` | date |  |
| `returnChannel.channelName` | string |  |
| `returnLineGroups[].groupNo` | number |  |
| `returnLineGroups[].returnExpectedFlag` | boolean |  |
| `returnOrderDate` | date |  |
| `returnOrderId` | string |  |
| `returnOrderLines[].cancellableQty` | number |  |
| `returnOrderLines[].charges[].chargeCategory` | string |  |
| `returnOrderLines[].charges[].chargeName` | string |  |
| `returnOrderLines[].charges[].chargePerUnit.currencyAmount` | number |  |
| `returnOrderLines[].charges[].chargePerUnit.currencyUnit` | string |  |
| `returnOrderLines[].charges[].excessCharge.currencyAmount` | number |  |
| `returnOrderLines[].charges[].excessCharge.currencyUnit` | string |  |
| `returnOrderLines[].charges[].isBillable` | boolean |  |
| `returnOrderLines[].charges[].isDiscount` | boolean |  |
| `returnOrderLines[].charges[].references[].name` | string |  |
| `returnOrderLines[].charges[].references[].value` | string |  |
| `returnOrderLines[].charges[].tax[].excessTax.currencyAmount` | number |  |
| `returnOrderLines[].charges[].tax[].excessTax.currencyUnit` | string |  |
| `returnOrderLines[].charges[].tax[].taxName` | string |  |
| `returnOrderLines[].charges[].tax[].taxPerUnit.currencyAmount` | number |  |
| `returnOrderLines[].charges[].tax[].taxPerUnit.currencyUnit` | string |  |
| `returnOrderLines[].chargeTotals[].name` | string |  |
| `returnOrderLines[].chargeTotals[].value.currencyAmount` | number |  |
| `returnOrderLines[].chargeTotals[].value.currencyUnit` | string |  |
| `returnOrderLines[].currentDeliveryStatus` | string |  |
| `returnOrderLines[].currentRefundStatus` | string |  |
| `returnOrderLines[].currentTrackingStatuses[].currentRefundStatus` | string |  |
| `returnOrderLines[].currentTrackingStatuses[].quantity.measurementValue` | number |  |
| `returnOrderLines[].currentTrackingStatuses[].quantity.unitOfMeasure` | string |  |
| `returnOrderLines[].currentTrackingStatuses[].status` | string |  |
| `returnOrderLines[].currentTrackingStatuses[].statusTime` | date |  |
| `returnOrderLines[].exceptionItemType` | string |  |
| `returnOrderLines[].isFastReplacement` | boolean |  |
| `returnOrderLines[].isKeepIt` | boolean |  |
| `returnOrderLines[].isReturnForException` | boolean |  |
| `returnOrderLines[].item.condition` | string |  |
| `returnOrderLines[].item.itemWeight.measurementValue` | number |  |
| `returnOrderLines[].item.itemWeight.unitOfMeasure` | string |  |
| `returnOrderLines[].item.productName` | string |  |
| `returnOrderLines[].item.sku` | string |  |
| `returnOrderLines[].lastItem` | boolean |  |
| `returnOrderLines[].purchaseOrderId` | string |  |
| `returnOrderLines[].purchaseOrderLineNumber` | number |  |
| `returnOrderLines[].quantity.measurementValue` | number |  |
| `returnOrderLines[].quantity.unitOfMeasure` | string |  |
| `returnOrderLines[].rechargeableQty` | number |  |
| `returnOrderLines[].rechargeReason` | string |  |
| `returnOrderLines[].refundChannels[].quantity.measurementValue` | number |  |
| `returnOrderLines[].refundChannels[].quantity.unitOfMeasure` | string |  |
| `returnOrderLines[].refundChannels[].refundChannelName` | string |  |
| `returnOrderLines[].refundCoveredBy` | string |  |
| `returnOrderLines[].refundedQty` | number |  |
| `returnOrderLines[].returnCancellationReason` | string |  |
| `returnOrderLines[].returnDescription` | string |  |
| `returnOrderLines[].returnExpectedFlag` | boolean |  |
| `returnOrderLines[].returnOrderLineNumber` | number |  |
| `returnOrderLines[].returnReason` | string |  |
| `returnOrderLines[].returnTrackingDetail[].eventDescription` | string |  |
| `returnOrderLines[].returnTrackingDetail[].eventTag` | string |  |
| `returnOrderLines[].returnTrackingDetail[].eventTime` | date |  |
| `returnOrderLines[].returnTrackingDetail[].references[].name` | string |  |
| `returnOrderLines[].returnTrackingDetail[].references[].value` | string |  |
| `returnOrderLines[].returnTrackingDetail[].sequenceNo` | number |  |
| `returnOrderLines[].salesOrderLineNumber` | number |  |
| `returnOrderLines[].sellerOrderId` | string |  |
| `returnOrderLines[].status` | string |  |
| `returnOrderLines[].statusTime` | date |  |
| `returnOrderLines[].unitPrice.currencyAmount` | number |  |
| `returnOrderLines[].unitPrice.currencyUnit` | string |  |
| `returnType` | string |  |
| `totalRefundAmount.currencyAmount` | number |  |
| `totalRefundAmount.currencyUnit` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST /v1/simulations/orders/:purchaseOrderId/deliver` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/simulate-order-delivery.md) for the provider-specific parameters and requirements.

