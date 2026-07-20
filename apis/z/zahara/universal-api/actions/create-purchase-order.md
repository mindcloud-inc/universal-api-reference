# Zahara: Create Purchase Order

Creates a new purchase order in Zahara.

```
POST https://connect.mindcloud.co/v1/universal/zahara/latest/actions/create-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/create-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requisitorId": 1,
  "totalNetValue": 1,
  "totalGrossValue": 1,
  "requiredDate": "2026-05-07T12:00:00.000Z",
  "documentId": 1,
  "businessDivisionId": 1,
  "supplierId": 1,
  "lineItem": {},
  "lineItems[]": [
    {}
  ],
  "currencyId": 1,
  "customFields[]": [
    {}
  ],
  "customFieldValues[]": [
    {}
  ],
  "lineItemId": 1,
  "lineItemDocumentId": 1,
  "lineItemProjectId": 1,
  "lineItemCostCodeId": 1,
  "lineItemQuantity": 1,
  "lineItemPrice": 1,
  "lineItemDescription": "string",
  "lineItemNominalCodeId": 1,
  "lineItemTaxCodeId": 1,
  "lineItemTaxPercentage": 1,
  "lineItemTaxValue": 1,
  "lineItemNetValue": 1,
  "lineItemQuantityReceived": 1,
  "lineItemDiscountPercentage": 1,
  "lineItemDivisionId": 1,
  "lineItemRequiredDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zahara/latest/actions/create-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requisitorId": 1,
    "totalNetValue": 1,
    "totalGrossValue": 1,
    "requiredDate": "2026-05-07T12:00:00.000Z",
    "documentId": 1,
    "businessDivisionId": 1,
    "supplierId": 1,
    "lineItem": {},
    "lineItems[]": [{}],
    "currencyId": 1,
    "customFields[]": [{}],
    "customFieldValues[]": [{}],
    "lineItemId": 1,
    "lineItemDocumentId": 1,
    "lineItemProjectId": 1,
    "lineItemCostCodeId": 1,
    "lineItemQuantity": 1,
    "lineItemPrice": 1,
    "lineItemDescription": "string",
    "lineItemNominalCodeId": 1,
    "lineItemTaxCodeId": 1,
    "lineItemTaxPercentage": 1,
    "lineItemTaxValue": 1,
    "lineItemNetValue": 1,
    "lineItemQuantityReceived": 1,
    "lineItemDiscountPercentage": 1,
    "lineItemDivisionId": 1,
    "lineItemRequiredDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requisitorId` | number | yes | Requisitor user ID. |
| `totalNetValue` | number | yes | Purchase order total net value. |
| `totalGrossValue` | number | yes | Purchase order total gross value. |
| `requiredDate` | date | yes | Required delivery date. |
| `documentId` | number | yes | Document ID for create payloads, usually 0. |
| `businessDivisionId` | number | yes | Business division ID. |
| `supplierId` | number | yes | Supplier ID. |
| `lineItem` | object | yes | First purchase order line item object. |
| `lineItems[]` | array<object> | yes | Purchase order line items. |
| `currencyId` | number | yes | Currency ID. |
| `customFields[]` | array<object> | yes | Custom fields array. |
| `customFieldValues[]` | array<object> | yes | Custom field values array. |
| `lineItemId` | number | yes | First line item ID, usually 0 for create. |
| `lineItemDocumentId` | number | yes | First line item document ID, usually 0 for create. |
| `lineItemProjectId` | number | yes | Project ID for the first line item. |
| `lineItemCostCodeId` | number | yes | Cost code ID for the first line item. |
| `lineItemQuantity` | number | yes | Quantity for the first line item. |
| `lineItemPrice` | number | yes | Price for the first line item. |
| `lineItemDescription` | string | yes | Description for the first line item. |
| `lineItemNominalCodeId` | number | yes | Nominal code ID for the first line item. |
| `lineItemTaxCodeId` | number | yes | Tax code ID for the first line item. |
| `lineItemTaxPercentage` | number | yes | Tax percentage for the first line item. |
| `lineItemTaxValue` | number | yes | Tax value for the first line item. |
| `lineItemNetValue` | number | yes | Net value for the first line item. |
| `lineItemQuantityReceived` | number | yes | Quantity received for the first line item. |
| `lineItemDiscountPercentage` | number | yes | Discount percentage for the first line item. |
| `lineItemDivisionId` | number | yes | Division ID for the first line item. |
| `lineItemRequiredDate` | date | yes | Required date for the first line item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "DocumentId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DocumentId` | number | Created purchase order document ID returned by Zahara. |

## Native endpoint

Through the native Zahara API, this operation is `POST /api/{{credentials.businessUnitApiKey}}/PurchaseOrder/Add` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order.md) for the provider-specific parameters and requirements.

