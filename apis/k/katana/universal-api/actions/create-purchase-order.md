# Katana: Create Purchase Order

Creates a new purchase order in Katana.

```
POST https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderNo": "string",
  "supplierId": 1,
  "locationId": 1,
  "purchaseOrderRows[]": [
    {}
  ],
  "purchaseOrderRows[].quantity": 1,
  "purchaseOrderRows[].variantId": 1,
  "purchaseOrderRows[].pricePerUnit": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderNo": "string",
    "supplierId": 1,
    "locationId": 1,
    "purchaseOrderRows[]": [{}],
    "purchaseOrderRows[].quantity": 1,
    "purchaseOrderRows[].variantId": 1,
    "purchaseOrderRows[].pricePerUnit": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderNo` | string | yes |  |
| `entityType` | string | no |  |
| `supplierId` | number | yes |  |
| `currency` | string | no | E.g. USD, EUR. All currently active currency codes in ISO 4217 format. |
| `status` | string | no |  |
| `expectedArrivalDate` | string | no |  |
| `orderCreatedDate` | string | no |  |
| `locationId` | number | yes |  |
| `trackingLocationId` | number | no | Submittable only when entity_type is outsourced |
| `additionalInfo` | string | no |  |
| `purchaseOrderRows[]` | array<object> | yes |  |
| `purchaseOrderRows[].quantity` | number | yes |  |
| `purchaseOrderRows[].variantId` | number | yes |  |
| `purchaseOrderRows[].taxRateId` | number | no |  |
| `purchaseOrderRows[].pricePerUnit` | number | yes |  |
| `purchaseOrderRows[].purchaseUomConversionRate` | number | no |  |
| `purchaseOrderRows[].purchaseUom` | string | no |  |
| `purchaseOrderRows[].arrivalDate` | string | no |  |

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
      "lastDocumentStatus": "string",
      "locationId": 1,
      "orderCreatedDate": "string",
      "orderNo": "string",
      "purchaseOrderRows": [
        {
          "batchTransactions": [
            "string"
          ],
          "conversionDate": "string",
          "conversionRate": "string",
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
| `lastDocumentStatus` | string |  |
| `locationId` | number |  |
| `orderCreatedDate` | string |  |
| `orderNo` | string |  |
| `purchaseOrderRows` | array<object> |  |
| `purchaseOrderRows[].batchTransactions` | array<string> |  |
| `purchaseOrderRows[].conversionDate` | string |  |
| `purchaseOrderRows[].conversionRate` | string |  |
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
| `supplierId` | number |  |
| `total` | number |  |
| `totalInBaseCurrency` | number |  |
| `trackingLocationId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `POST /purchase_orders` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order.md) for the provider-specific parameters and requirements.

