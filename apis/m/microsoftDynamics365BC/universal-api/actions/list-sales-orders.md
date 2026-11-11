# Microsoft Dynamics 365 BC: List Sales Orders



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/list-sales-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/list-sales-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/list-sales-orders?${params}`, {
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
| `companyId` | list<string> | yes | The Business Central company that holds the sales orders. |
| `filter` | string | no | Optional OData filter on sales order fields, such as number, customerNumber, status or lastModifiedDateTime. Example: customerNumber eq '10000' and totalAmountIncludingTax gt 1000 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billToAddressLine1": "string",
      "billToAddressLine2": "string",
      "billToCity": "string",
      "billToCountry": "string",
      "billToCustomerId": "string",
      "billToCustomerNumber": "string",
      "billToName": "Ava Chen",
      "billToPostCode": "string",
      "billToState": "string",
      "currencyCode": "string",
      "currencyId": "string",
      "customerId": "string",
      "customerName": "Ava Chen",
      "customerNumber": "string",
      "discountAmount": 1,
      "discountAppliedBeforeTax": true,
      "email": "ava@example.com",
      "externalDocumentNumber": "string",
      "fullyShipped": true,
      "id": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "number": "string",
      "orderDate": "2026-05-07T12:00:00.000Z",
      "partialShipping": true,
      "paymentTermsId": "string",
      "phoneNumber": "string",
      "postingDate": "2026-05-07T12:00:00.000Z",
      "pricesIncludeTax": true,
      "requestedDeliveryDate": "2026-05-07T12:00:00.000Z",
      "salesperson": "string",
      "sellToAddressLine1": "string",
      "sellToAddressLine2": "string",
      "sellToCity": "string",
      "sellToCountry": "string",
      "sellToPostCode": "string",
      "sellToState": "string",
      "shipmentMethodId": "string",
      "shipToAddressLine1": "string",
      "shipToAddressLine2": "string",
      "shipToCity": "string",
      "shipToContact": "string",
      "shipToCountry": "string",
      "shipToName": "Ava Chen",
      "shipToPostCode": "string",
      "shipToState": "string",
      "shortcutDimension1Code": "string",
      "shortcutDimension2Code": "string",
      "status": "string",
      "totalAmountExcludingTax": 1,
      "totalAmountIncludingTax": 1,
      "totalTaxAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billToAddressLine1` | string |  |
| `billToAddressLine2` | string |  |
| `billToCity` | string |  |
| `billToCountry` | string |  |
| `billToCustomerId` | string |  |
| `billToCustomerNumber` | string |  |
| `billToName` | string |  |
| `billToPostCode` | string |  |
| `billToState` | string |  |
| `currencyCode` | string |  |
| `currencyId` | string |  |
| `customerId` | string |  |
| `customerName` | string |  |
| `customerNumber` | string |  |
| `discountAmount` | number |  |
| `discountAppliedBeforeTax` | boolean |  |
| `email` | string |  |
| `externalDocumentNumber` | string |  |
| `fullyShipped` | boolean |  |
| `id` | string |  |
| `lastModifiedDateTime` | date |  |
| `number` | string |  |
| `orderDate` | date |  |
| `partialShipping` | boolean |  |
| `paymentTermsId` | string |  |
| `phoneNumber` | string |  |
| `postingDate` | date |  |
| `pricesIncludeTax` | boolean |  |
| `requestedDeliveryDate` | date |  |
| `salesperson` | string |  |
| `sellToAddressLine1` | string |  |
| `sellToAddressLine2` | string |  |
| `sellToCity` | string |  |
| `sellToCountry` | string |  |
| `sellToPostCode` | string |  |
| `sellToState` | string |  |
| `shipmentMethodId` | string |  |
| `shipToAddressLine1` | string |  |
| `shipToAddressLine2` | string |  |
| `shipToCity` | string |  |
| `shipToContact` | string |  |
| `shipToCountry` | string |  |
| `shipToName` | string |  |
| `shipToPostCode` | string |  |
| `shipToState` | string |  |
| `shortcutDimension1Code` | string |  |
| `shortcutDimension2Code` | string |  |
| `status` | string |  |
| `totalAmountExcludingTax` | number |  |
| `totalAmountIncludingTax` | number |  |
| `totalTaxAmount` | number |  |

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `GET v2.0/companies(:companyId)/salesOrders` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-orders.md) for the provider-specific parameters and requirements.

