# Zahara: Update Purchase Order

Updates an existing purchase order in Zahara.

```
PUT https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "14085496",
  "lineItem": {},
  "requisitorId": 1,
  "totalNetValue": 1,
  "totalGrossValue": 1,
  "requiredDate": "2026-05-07T12:00:00.000Z",
  "documentBodyId": 1,
  "businessDivisionId": 1,
  "supplierId": 1,
  "currencyId": 1,
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
  "lineItemDivisionId": 1,
  "lineItemRequiredDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-purchase-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "14085496",
    "lineItem": {},
    "requisitorId": 1,
    "totalNetValue": 1,
    "totalGrossValue": 1,
    "requiredDate": "2026-05-07T12:00:00.000Z",
    "documentBodyId": 1,
    "businessDivisionId": 1,
    "supplierId": 1,
    "currencyId": 1,
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
| `documentId` | number | yes | Purchase order document ID to update. Example: `14085496`. |
| `lineItem` | object | yes | First purchase order line item object. |
| `requisitorId` | number | yes | Requisitor user ID. |
| `totalNetValue` | number | yes | Purchase order total net value. |
| `totalGrossValue` | number | yes | Purchase order total gross value. |
| `requiredDate` | date | yes | Required delivery date. |
| `documentBodyId` | number | yes | Document ID echoed in the update body. |
| `businessDivisionId` | number | yes | Business division ID. |
| `supplierId` | number | yes | Supplier ID. |
| `currencyId` | number | yes | Currency ID. |
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
| `DocumentId` | number | Purchase order document ID represented for successful update operations in MindCloud. |

## Native endpoint

Through the native Zahara API, this operation is `PUT /api/{{credentials.businessUnitApiKey}}/PurchaseOrder/Update/{{documentId}}` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-purchase-order.md) for the provider-specific parameters and requirements.

