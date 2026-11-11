# Microsoft Dynamics 365 BC: List Sales Order Lines



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/list-sales-order-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/list-sales-order-lines?connectionId=$CONNECTION_ID&limit=25&offset=0&companyId=string&salesOrderId=5d115c9c-44e3-ea11-bb43-000d3a2feca1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyId": "string",
  "salesOrderId": "5d115c9c-44e3-ea11-bb43-000d3a2feca1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/list-sales-order-lines?${params}`, {
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
| `companyId` | list<string> | yes | The Business Central company that holds the sales order. |
| `salesOrderId` | string | yes | The sales order's system ID (GUID), not the order number. Example: `5d115c9c-44e3-ea11-bb43-000d3a2feca1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "amountExcludingTax": 1,
      "amountIncludingTax": 1,
      "description": "string",
      "description2": "string",
      "discountAmount": 1,
      "discountAppliedBeforeTax": true,
      "discountPercent": 1,
      "documentId": "string",
      "id": "string",
      "invoiceDiscountAllocation": 1,
      "invoicedQuantity": 1,
      "invoiceQuantity": 1,
      "itemId": "string",
      "itemVariantId": "string",
      "lineObjectNumber": "string",
      "lineType": "string",
      "locationId": "string",
      "netAmount": 1,
      "netAmountIncludingTax": 1,
      "netTaxAmount": 1,
      "quantity": 1,
      "sequence": 1,
      "shipmentDate": "2026-05-07T12:00:00.000Z",
      "shippedQuantity": 1,
      "shipQuantity": 1,
      "taxCode": "string",
      "taxPercent": 1,
      "totalTaxAmount": 1,
      "unitOfMeasureCode": "string",
      "unitOfMeasureId": "string",
      "unitPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `amountExcludingTax` | number |  |
| `amountIncludingTax` | number |  |
| `description` | string |  |
| `description2` | string |  |
| `discountAmount` | number |  |
| `discountAppliedBeforeTax` | boolean |  |
| `discountPercent` | number |  |
| `documentId` | string |  |
| `id` | string |  |
| `invoiceDiscountAllocation` | number |  |
| `invoicedQuantity` | number |  |
| `invoiceQuantity` | number |  |
| `itemId` | string |  |
| `itemVariantId` | string |  |
| `lineObjectNumber` | string |  |
| `lineType` | string |  |
| `locationId` | string |  |
| `netAmount` | number |  |
| `netAmountIncludingTax` | number |  |
| `netTaxAmount` | number |  |
| `quantity` | number |  |
| `sequence` | number |  |
| `shipmentDate` | date |  |
| `shippedQuantity` | number |  |
| `shipQuantity` | number |  |
| `taxCode` | string |  |
| `taxPercent` | number |  |
| `totalTaxAmount` | number |  |
| `unitOfMeasureCode` | string |  |
| `unitOfMeasureId` | string |  |
| `unitPrice` | number |  |

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `GET v2.0/companies(:companyId)/salesOrders(:salesOrderId)/salesOrderLines` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-order-lines.md) for the provider-specific parameters and requirements.

