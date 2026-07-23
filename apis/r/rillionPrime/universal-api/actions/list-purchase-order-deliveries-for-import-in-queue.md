# Rillion Prime: List Purchase Order Deliveries For Import In Queue



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-purchase-order-deliveries-for-import-in-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-purchase-order-deliveries-for-import-in-queue?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-purchase-order-deliveries-for-import-in-queue?${params}`, {
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
| `queueStatus` | number | no | Request body value for QueueStatus. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "purchaseOrderDeliveryModel": {
        "company": "string",
        "deliveryDate": "string",
        "deliveryNote": "string",
        "purchaseOrderDeliveryLines": [
          {
            "amount": 1,
            "lineNo": "string",
            "number": 1,
            "purchaseOrderNo": "string",
            "queueStatus": 1,
            "queueType": 1
          }
        ],
        "queueStatus": 1,
        "queueType": 1,
        "supplier": "string",
        "supplierDeliveryNote": "string"
      },
      "supplier": "string",
      "supplierDeliveryNote": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `purchaseOrderDeliveryModel.company` | string |  |
| `purchaseOrderDeliveryModel.deliveryDate` | string |  |
| `purchaseOrderDeliveryModel.deliveryNote` | string |  |
| `purchaseOrderDeliveryModel.purchaseOrderDeliveryLines[].amount` | number |  |
| `purchaseOrderDeliveryModel.purchaseOrderDeliveryLines[].lineNo` | string |  |
| `purchaseOrderDeliveryModel.purchaseOrderDeliveryLines[].number` | number |  |
| `purchaseOrderDeliveryModel.purchaseOrderDeliveryLines[].purchaseOrderNo` | string |  |
| `purchaseOrderDeliveryModel.purchaseOrderDeliveryLines[].queueStatus` | number |  |
| `purchaseOrderDeliveryModel.purchaseOrderDeliveryLines[].queueType` | number |  |
| `purchaseOrderDeliveryModel.queueStatus` | number |  |
| `purchaseOrderDeliveryModel.queueType` | number |  |
| `purchaseOrderDeliveryModel.supplier` | string |  |
| `purchaseOrderDeliveryModel.supplierDeliveryNote` | string |  |
| `supplier` | string |  |
| `supplierDeliveryNote` | string |  |

## Native endpoint

Through the native Rillion Prime API, this operation is `POST /purchaseorderdeliveryqueue/ListPurchaseOrderDeliveryForImportInQueue` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-purchase-order-deliveries-for-import-in-queue.md) for the provider-specific parameters and requirements.

