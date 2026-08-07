# ShipBob: Get Return Order



```
GET https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/get-return-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipBob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/get-return-order?connectionId=$CONNECTION_ID&id=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/get-return-order?${params}`, {
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
| `id` | number | yes | The ShipBob return order ID. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "arrivedDate": "string",
      "awaitingArrivalDate": "string",
      "cancelledDate": {},
      "channel": {
        "id": 1,
        "name": "Ava Chen"
      },
      "completedDate": "string",
      "customerName": {},
      "fulfillmentCenter": {
        "id": 1,
        "name": "Ava Chen"
      },
      "id": 1,
      "insertDate": "string",
      "inventory": [
        {
          "actionRequested": {
            "action": "string",
            "actionType": "string",
            "instructions": "string"
          },
          "actionTaken": [
            {
              "action": "string",
              "actionReason": {},
              "imageUrl": {},
              "quantityProcessed": 1
            }
          ],
          "barcodes": [
            "string"
          ],
          "bundleParentSku": {},
          "id": 1,
          "lotInformation": {},
          "name": "Ava Chen",
          "quantityExpected": 1,
          "quantityProcessed": 1,
          "sku": "string"
        }
      ],
      "invoice": {
        "amount": 1,
        "currencyCode": "string"
      },
      "originalShipmentId": 1,
      "processingDate": "string",
      "referenceId": "string",
      "returnType": "string",
      "shipmentTrackingNumber": "string",
      "status": "string",
      "statusHistory": [
        {
          "status": "string",
          "timestamp": "string"
        }
      ],
      "storeOrderId": "string",
      "trackingNumber": "string",
      "transactions": [
        {
          "amount": 1,
          "transactionType": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arrivedDate` | string |  |
| `awaitingArrivalDate` | string |  |
| `cancelledDate` | object |  |
| `channel.id` | number |  |
| `channel.name` | string |  |
| `completedDate` | string |  |
| `customerName` | object |  |
| `fulfillmentCenter.id` | number |  |
| `fulfillmentCenter.name` | string |  |
| `id` | number |  |
| `insertDate` | string |  |
| `inventory[].actionRequested.action` | string |  |
| `inventory[].actionRequested.actionType` | string |  |
| `inventory[].actionRequested.instructions` | string |  |
| `inventory[].actionTaken[].action` | string |  |
| `inventory[].actionTaken[].actionReason` | object |  |
| `inventory[].actionTaken[].imageUrl` | object |  |
| `inventory[].actionTaken[].quantityProcessed` | number |  |
| `inventory[].barcodes[]` | string |  |
| `inventory[].bundleParentSku` | object |  |
| `inventory[].id` | number |  |
| `inventory[].lotInformation` | object |  |
| `inventory[].name` | string |  |
| `inventory[].quantityExpected` | number |  |
| `inventory[].quantityProcessed` | number |  |
| `inventory[].sku` | string |  |
| `invoice.amount` | number |  |
| `invoice.currencyCode` | string |  |
| `originalShipmentId` | number |  |
| `processingDate` | string |  |
| `referenceId` | string |  |
| `returnType` | string |  |
| `shipmentTrackingNumber` | string |  |
| `status` | string |  |
| `statusHistory[].status` | string |  |
| `statusHistory[].timestamp` | string |  |
| `storeOrderId` | string |  |
| `trackingNumber` | string |  |
| `transactions[].amount` | number |  |
| `transactions[].transactionType` | string |  |

## Native endpoint

Through the native ShipBob API, this operation is `GET 2026-07/return/:id` (base URL `https://{{credentials.apiSubdomain}}.shipbob.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-return-order.md) for the provider-specific parameters and requirements.

