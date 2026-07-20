# Lightspeed Retail POS (X-Series): List Sales

Retrieves sales from Lightspeed Retail POS (X-Series).

```
GET https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-sales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-sales?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "customer": {},
      "customerId": "string",
      "deletedAt": "string",
      "id": "string",
      "invoiceNumber": "string",
      "invoiceSequence": "string",
      "lineItems": [
        {}
      ],
      "note": "string",
      "outletId": "string",
      "receiptNumber": "string",
      "receiptSequence": "string",
      "registerId": "string",
      "registerSaleAttributes": [
        "string"
      ],
      "registerSalePayments": [
        {}
      ],
      "registerSaleProducts": [
        {}
      ],
      "returnFor": "string",
      "saleDate": "string",
      "shortCode": "string",
      "state": "string",
      "status": "string",
      "taxes": [
        {}
      ],
      "taxName": "Ava Chen",
      "totalCost": "string",
      "totalLoyalty": "string",
      "totalPrice": "string",
      "totals": {},
      "totalTax": "string",
      "updatedAt": "string",
      "userId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `customer` | object | Embedded customer object when included. |
| `customerId` | string | Customer ID associated with the sale. |
| `deletedAt` | string | Deletion timestamp. |
| `id` | string | Sale ID from the sale object example. |
| `invoiceNumber` | string | Invoice number for the sale. |
| `invoiceSequence` | string | Invoice sequence value. |
| `lineItems` | array<object> | Line items array. |
| `note` | string | Sale note. |
| `outletId` | string | Outlet ID for the sale. |
| `receiptNumber` | string | Receipt number for the sale. |
| `receiptSequence` | string | Receipt sequence value. |
| `registerId` | string | Register ID for the sale. |
| `registerSaleAttributes` | array<string> | Sale attributes. |
| `registerSalePayments` | array<object> | Sale payments array. |
| `registerSaleProducts` | array<object> | Legacy sale line items array. |
| `returnFor` | string | Original sale ID when this is a return. |
| `saleDate` | string | Sale timestamp. |
| `shortCode` | string | Short sale code. |
| `state` | string | Current sale state. |
| `status` | string | Deprecated sale status. |
| `taxes` | array<object> | Tax breakdown array. |
| `taxName` | string | Tax name. |
| `totalCost` | string | Total sale cost. |
| `totalLoyalty` | string | Total loyalty amount. |
| `totalPrice` | string | Total sale price. |
| `totals` | object | Aggregated totals object. |
| `totalTax` | string | Total sale tax. |
| `updatedAt` | string | Update timestamp. |
| `userId` | string | User ID associated with the sale. |
| `userName` | string | User name associated with the sale. |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `GET /api/2.0/sales` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales.md) for the provider-specific parameters and requirements.

