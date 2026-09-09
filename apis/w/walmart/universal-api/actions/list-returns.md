# Walmart: List Returns

Retrieve details for return orders that match the filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-returns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-returns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-returns?${params}`, {
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
| `status` | list<string> | no | Example: `INITIATED`. |
| `returnType` | list<string> | no | Example: `REFUND`. |
| `returnOrderId` | string | no |  |
| `customerOrderId` | string | no |  |
| `returnCreationStartDate` | date | no | Example: `2020-03-16 or 2020-03-16T10:30:15Z`. |
| `returnCreationEndDate` | date | no | Example: `2020-03-16 or 2020-03-16T10:30:15Z`. |
| `returnLastModifiedStartDate` | date | no | Example: `2020-03-16 or 2020-03-16T10:30:15Z`. |
| `returnLastModifiedEndDate` | date | no | Example: `2020-03-16 or 2020-03-16T10:30:15Z`. |
| `replacementInfo` | boolean | no | Example: `replacementCustomerOrderID`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dynamicSandbox` | boolean | no |  |

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
      "refundMode": "string",
      "replacementCustomerOrderId": "string",
      "returnByDate": "2026-05-07T12:00:00.000Z",
      "returnChannel": {
        "channelName": "Ava Chen"
      },
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
          "isFastReplacement": true,
          "isKeepIt": true,
          "isReturnForException": true,
          "item": {
            "condition": "string",
            "itemWeight": {
              "measurementValue": 1,
              "unitOfMeasure": "string"
            },
            "productName": "Ava Chen"
          },
          "lastItem": true,
          "purchaseOrderId": "string",
          "purchaseOrderLineNumber": 1,
          "quantity": {
            "measurementValue": 1,
            "unitOfMeasure": "string"
          },
          "rechargeableQty": 1,
          "refundChannels": [
            {
              "quantity": {
                "measurementValue": 1
              },
              "refundChannelName": "Ava Chen"
            }
          ],
          "refundCoveredBy": "string",
          "refundedQty": 1,
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
| `refundMode` | string |  |
| `replacementCustomerOrderId` | string |  |
| `returnByDate` | date |  |
| `returnChannel.channelName` | string |  |
| `returnOrderDate` | date |  |
| `returnOrderId` | string |  |
| `returnOrderLines[].cancellableQty` | number |  |
| `returnOrderLines[].charges[].chargeCategory` | string |  |
| `returnOrderLines[].charges[].chargeName` | string |  |
| `returnOrderLines[].charges[].chargePerUnit.currencyAmount` | number |  |
| `returnOrderLines[].charges[].chargePerUnit.currencyUnit` | string |  |
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
| `returnOrderLines[].isFastReplacement` | boolean |  |
| `returnOrderLines[].isKeepIt` | boolean |  |
| `returnOrderLines[].isReturnForException` | boolean |  |
| `returnOrderLines[].item.condition` | string |  |
| `returnOrderLines[].item.itemWeight.measurementValue` | number |  |
| `returnOrderLines[].item.itemWeight.unitOfMeasure` | string |  |
| `returnOrderLines[].item.productName` | string |  |
| `returnOrderLines[].lastItem` | boolean |  |
| `returnOrderLines[].purchaseOrderId` | string |  |
| `returnOrderLines[].purchaseOrderLineNumber` | number |  |
| `returnOrderLines[].quantity.measurementValue` | number |  |
| `returnOrderLines[].quantity.unitOfMeasure` | string |  |
| `returnOrderLines[].rechargeableQty` | number |  |
| `returnOrderLines[].refundChannels[].quantity.measurementValue` | number |  |
| `returnOrderLines[].refundChannels[].refundChannelName` | string |  |
| `returnOrderLines[].refundCoveredBy` | string |  |
| `returnOrderLines[].refundedQty` | number |  |
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
| `returnOrderLines[].status` | string |  |
| `returnOrderLines[].statusTime` | date |  |
| `returnOrderLines[].unitPrice.currencyAmount` | number |  |
| `returnOrderLines[].unitPrice.currencyUnit` | string |  |
| `returnType` | string |  |
| `totalRefundAmount.currencyAmount` | number |  |
| `totalRefundAmount.currencyUnit` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/returns` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-returns.md) for the provider-specific parameters and requirements.

