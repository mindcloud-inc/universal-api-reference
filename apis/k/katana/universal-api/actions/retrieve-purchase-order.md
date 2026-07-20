# Katana: Retrieve Purchase Order

Retrieves a purchase order by ID from Katana.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-purchase-order?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-purchase-order?${params}`, {
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
| `id` | number | yes | Purchase order id |
| `extend[]` | array<string> | no | Array of objects that need to be added to the response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalInfo": "string",
      "billingStatus": "string",
      "createdAt": "string",
      "currency": "string",
      "defaultGroupId": 1,
      "deletedAt": "string",
      "entityType": "string",
      "expectedArrivalDate": "string",
      "id": 1,
      "ingredientAvailability": "string",
      "ingredientExpectedDate": "string",
      "lastDocumentStatus": "string",
      "locationId": 1,
      "orderCreatedDate": "string",
      "orderNo": "string",
      "purchaseOrderRows": [
        {
          "batchTransactions": [
            {
              "batchId": 1,
              "quantity": 1
            }
          ],
          "conversionDate": "string",
          "conversionRate": 1,
          "createdAt": "string",
          "currency": "string",
          "deletedAt": "string",
          "groupId": 1,
          "id": 1,
          "landedCost": "string",
          "pricePerUnit": 1,
          "purchaseOrderId": 1,
          "purchaseUom": "string",
          "purchaseUomConversionRate": 1,
          "quantity": 1,
          "receivedDate": "string",
          "taxRateId": 1,
          "total": 1,
          "totalInBaseCurrency": 1,
          "updatedAt": "string",
          "variantId": 1
        }
      ],
      "status": "string",
      "supplier": {
        "comment": "string",
        "createdAt": "string",
        "currency": "string",
        "deletedAt": "string",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "updatedAt": "string"
      },
      "supplierId": 1,
      "total": 1,
      "totalInBaseCurrency": 1,
      "trackingLocationId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalInfo` | string |  |
| `billingStatus` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `defaultGroupId` | number |  |
| `deletedAt` | string |  |
| `entityType` | string |  |
| `expectedArrivalDate` | string |  |
| `id` | number |  |
| `ingredientAvailability` | string |  |
| `ingredientExpectedDate` | string |  |
| `lastDocumentStatus` | string |  |
| `locationId` | number |  |
| `orderCreatedDate` | string |  |
| `orderNo` | string |  |
| `purchaseOrderRows` | array<object> |  |
| `purchaseOrderRows[].batchTransactions` | array<object> |  |
| `purchaseOrderRows[].batchTransactions[].batchId` | number |  |
| `purchaseOrderRows[].batchTransactions[].quantity` | number |  |
| `purchaseOrderRows[].conversionDate` | string |  |
| `purchaseOrderRows[].conversionRate` | number |  |
| `purchaseOrderRows[].createdAt` | string |  |
| `purchaseOrderRows[].currency` | string |  |
| `purchaseOrderRows[].deletedAt` | string |  |
| `purchaseOrderRows[].groupId` | number |  |
| `purchaseOrderRows[].id` | number |  |
| `purchaseOrderRows[].landedCost` | string |  |
| `purchaseOrderRows[].pricePerUnit` | number |  |
| `purchaseOrderRows[].purchaseOrderId` | number |  |
| `purchaseOrderRows[].purchaseUom` | string |  |
| `purchaseOrderRows[].purchaseUomConversionRate` | number |  |
| `purchaseOrderRows[].quantity` | number |  |
| `purchaseOrderRows[].receivedDate` | string |  |
| `purchaseOrderRows[].taxRateId` | number |  |
| `purchaseOrderRows[].total` | number |  |
| `purchaseOrderRows[].totalInBaseCurrency` | number |  |
| `purchaseOrderRows[].updatedAt` | string |  |
| `purchaseOrderRows[].variantId` | number |  |
| `status` | string |  |
| `supplier` | object |  |
| `supplier.comment` | string |  |
| `supplier.createdAt` | string |  |
| `supplier.currency` | string |  |
| `supplier.deletedAt` | string |  |
| `supplier.email` | string |  |
| `supplier.id` | number |  |
| `supplier.name` | string |  |
| `supplier.updatedAt` | string |  |
| `supplierId` | number |  |
| `total` | number |  |
| `totalInBaseCurrency` | number |  |
| `trackingLocationId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `GET /purchase_orders/:id` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-purchase-order.md) for the provider-specific parameters and requirements.

