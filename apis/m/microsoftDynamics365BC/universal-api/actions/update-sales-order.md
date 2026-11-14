# Microsoft Dynamics 365 BC: Update Sales Order



```
PUT https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "salesOrderId": "5d115c9c-44e3-ea11-bb43-000d3a2feca1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-sales-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string",
    "salesOrderId": "5d115c9c-44e3-ea11-bb43-000d3a2feca1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billToCustomerId` | string | no | The ID (GUID) of the bill-to customer. |
| `billToCustomerNumber` | string | no | The number of the bill-to customer. |
| `companyId` | list<string> | yes | The Business Central company that holds the sales order. |
| `currencyCode` | string | no | The currency code for the sales order. |
| `currencyId` | string | no | The ID (GUID) of the currency the sales order uses. |
| `customerId` | string | no | The ID (GUID) of the sell-to customer. |
| `customerNumber` | string | no | The number of the sell-to customer. |
| `discountAmount` | number | no | The sales order discount amount. |
| `email` | string | no | The sales order's email address. |
| `externalDocumentNumber` | string | no | An external document number for the sales order, such as the customer's PO number. |
| `orderDate` | string | no | The order date, in YYYY-MM-DD format. |
| `partialShipping` | boolean | no | Whether partial shipping of items is preferred. |
| `paymentTermsId` | string | no | The ID (GUID) of the payment terms the sales order uses. |
| `phoneNumber` | string | no | The sales order's telephone number. |
| `postingDate` | string | no | The date the sales order is posted, in YYYY-MM-DD format. |
| `requestedDeliveryDate` | string | no | The requested delivery date, in YYYY-MM-DD format. |
| `salesOrderId` | string | yes | The sales order's system ID (GUID), not the order number. Example: `5d115c9c-44e3-ea11-bb43-000d3a2feca1`. |
| `salesperson` | string | no | The salesperson code for the sales order. |
| `sellToAddressLine1` | string | no | Sell-to address line 1. |
| `sellToAddressLine2` | string | no | Sell-to address line 2. |
| `sellToCity` | string | no | Sell-to city. |
| `sellToCountry` | string | no | Sell-to country/region code. |
| `sellToPostCode` | string | no | Sell-to post code. |
| `sellToState` | string | no | Sell-to state. |
| `shipmentMethodId` | string | no | The ID (GUID) of the shipment method the sales order uses. |
| `shipToAddressLine1` | string | no | Ship-to address line 1. |
| `shipToAddressLine2` | string | no | Ship-to address line 2. |
| `shipToCity` | string | no | Ship-to city. |
| `shipToContact` | string | no | The ship-to contact. |
| `shipToCountry` | string | no | Ship-to country/region code. |
| `shipToName` | string | no | The ship-to name. |
| `shipToPostCode` | string | no | Ship-to post code. |
| `shipToState` | string | no | Ship-to state. |
| `shortcutDimension1Code` | string | no | The code for shortcut dimension 1. |
| `shortcutDimension2Code` | string | no | The code for shortcut dimension 2. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `PATCH v2.0/companies(:companyId)/salesOrders(:salesOrderId)` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-order.md) for the provider-specific parameters and requirements.

