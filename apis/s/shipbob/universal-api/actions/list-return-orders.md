# ShipBob: List Return Orders



```
GET https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/list-return-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipBob `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/list-return-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/list-return-orders?${params}`, {
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
| `ids` | string | no | Comma-separated return order IDs. Accepts multiple values in one string, delimited by `,`. Example: `123,456,789`. |
| `referenceIds` | string | no | Comma-separated return reference IDs or RMA numbers. Accepts multiple values in one string, delimited by `,`. Example: `RMA-1001,RMA-1002`. |
| `status` | list<string> | no | One or more return statuses: AwaitingArrival, Arrived, Processing, Completed, or Cancelled. One of: `Arrived`, `AwaitingArrival`, `Cancelled`, `Completed`, `Processing`. Accepts multiple values in one string, delimited by `,`. |
| `trackingNumbers` | string | no | Comma-separated return tracking numbers. Accepts multiple values in one string, delimited by `,`. Example: `1Z9999W99999999999`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fulfillmentCenterIds` | list<number> | no | Comma-separated fulfillment center IDs. Accepts multiple values in one string, delimited by `,`. |
| `originalShipmentIds` | string | no | Comma-separated original shipment IDs. Accepts multiple values in one string, delimited by `,`. Example: `123456,123457`. |
| `inventoryIds` | list<number> | no | Comma-separated inventory IDs. Accepts multiple values in one string, delimited by `,`. |
| `startDate` | date | no | Return orders created on or after this ISO 8601 date and time. |
| `endDate` | date | no | Return orders created on or before this ISO 8601 date and time. |
| `returnTypes` | list<string> | no | Comma-separated return types, such as Regular or ReturnToSender. One of: `Regular`, `ReturnToSender`. Accepts multiple values in one string, delimited by `,`. |
| `returnActions` | list<string> | no | Comma-separated requested actions, such as Restock, Quarantine, or Dispose. One of: `Default`, `Dispose`, `Quarantine`, `Restock`. Accepts multiple values in one string, delimited by `,`. |
| `storeOrderIds` | string | no | Comma-separated store order IDs. Accepts multiple values in one string, delimited by `,`. Example: `ORDER-1001,ORDER-1002`. |
| `completedStartDate` | date | no | Return orders completed on or after this ISO 8601 date and time. |
| `completedEndDate` | date | no | Return orders completed on or before this ISO 8601 date and time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "arrivedDate": "string",
      "awaitingArrivalDate": "string",
      "cancelledDate": {},
      "channel": {},
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
          "id": 1,
          "lotInformation": {},
          "name": "Ava Chen",
          "quantity": 1,
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
| `channel` | object |  |
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
| `inventory[].id` | number |  |
| `inventory[].lotInformation` | object |  |
| `inventory[].name` | string |  |
| `inventory[].quantity` | number |  |
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

Through the native ShipBob API, this operation is `GET 2026-07/return` (base URL `https://{{credentials.apiSubdomain}}.shipbob.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-return-orders.md) for the provider-specific parameters and requirements.

