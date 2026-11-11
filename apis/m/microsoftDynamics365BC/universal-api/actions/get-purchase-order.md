# Microsoft Dynamics 365 BC: Get Purchase Order



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/get-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/get-purchase-order?connectionId=$CONNECTION_ID&companyId=string&purchaseOrderId=5d115c9c-44e3-ea11-bb43-000d3a2feca1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string",
  "purchaseOrderId": "5d115c9c-44e3-ea11-bb43-000d3a2feca1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/get-purchase-order?${params}`, {
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
| `companyId` | list<string> | yes | The Business Central company that holds the purchase order. |
| `purchaseOrderId` | string | yes | The purchase order's system ID (GUID), not the order number. Example: `5d115c9c-44e3-ea11-bb43-000d3a2feca1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buyFromAddressLine1": "string",
      "buyFromAddressLine2": "string",
      "buyFromCity": "string",
      "buyFromCountry": "string",
      "buyFromPostCode": "string",
      "buyFromState": "string",
      "currencyCode": "string",
      "currencyId": "string",
      "discountAmount": 1,
      "discountAppliedBeforeTax": true,
      "fullyReceived": true,
      "id": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "number": "string",
      "orderDate": "2026-05-07T12:00:00.000Z",
      "paymentTermsId": "string",
      "payToAddressLine1": "string",
      "payToAddressLine2": "string",
      "payToCity": "string",
      "payToCountry": "string",
      "payToName": "Ava Chen",
      "payToPostCode": "string",
      "payToState": "string",
      "payToVendorId": "string",
      "payToVendorNumber": "string",
      "postingDate": "2026-05-07T12:00:00.000Z",
      "pricesIncludeTax": true,
      "purchaser": "string",
      "requestedReceiptDate": "2026-05-07T12:00:00.000Z",
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
      "totalTaxAmount": 1,
      "vendorId": "string",
      "vendorName": "Ava Chen",
      "vendorNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buyFromAddressLine1` | string |  |
| `buyFromAddressLine2` | string |  |
| `buyFromCity` | string |  |
| `buyFromCountry` | string |  |
| `buyFromPostCode` | string |  |
| `buyFromState` | string |  |
| `currencyCode` | string |  |
| `currencyId` | string |  |
| `discountAmount` | number |  |
| `discountAppliedBeforeTax` | boolean |  |
| `fullyReceived` | boolean |  |
| `id` | string |  |
| `lastModifiedDateTime` | date |  |
| `number` | string |  |
| `orderDate` | date |  |
| `paymentTermsId` | string |  |
| `payToAddressLine1` | string |  |
| `payToAddressLine2` | string |  |
| `payToCity` | string |  |
| `payToCountry` | string |  |
| `payToName` | string |  |
| `payToPostCode` | string |  |
| `payToState` | string |  |
| `payToVendorId` | string |  |
| `payToVendorNumber` | string |  |
| `postingDate` | date |  |
| `pricesIncludeTax` | boolean |  |
| `purchaser` | string |  |
| `requestedReceiptDate` | date |  |
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
| `vendorId` | string |  |
| `vendorName` | string |  |
| `vendorNumber` | string |  |

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `GET v2.0/companies(:companyId)/purchaseOrders(:purchaseOrderId)` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-order.md) for the provider-specific parameters and requirements.

