# Microsoft Dynamics 365 BC: Create Sales Order



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-sales-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no |  |
| `orderDate` | string | no |  |
| `customerId` | string | no |  |
| `externalDocumentNumber` | string | no |  |
| `billToAddressLine1` | string | no |  |
| `currencyCode` | string | no |  |
| `customerName` | string | no |  |
| `customerNumber` | string | no |  |
| `discountAmount` | number | no |  |
| `discountAppliedBeforeTax` | boolean | no |  |
| `documentLines[]` | array | no |  |
| `email` | string | no |  |
| `fullyShipped` | boolean | no |  |
| `lastModifiedDateTime` | string | no |  |
| `partialShipping` | boolean | no |  |
| `paymentTermsId` | string | no |  |
| `phoneNumber` | string | no |  |
| `postingDate` | string | no |  |
| `pricesIncludeTax` | boolean | no |  |
| `requestedDeliveryDate` | string | no |  |
| `salesperson` | string | no |  |
| `sellToAddressLine1` | string | no |  |
| `shipmentMethodId` | string | no |  |
| `shipToName` | string | no |  |
| `shortcutDimension1Code` | string | no |  |
| `shortcutDimension2Code` | string | no |  |
| `status` | string | no |  |
| `totalAmountExcludingTax` | number | no |  |
| `totalAmountIncludingTax` | number | no |  |
| `totalTaxAmount` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `POST companies(:id)/salesOrders` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-order.md) for the provider-specific parameters and requirements.

