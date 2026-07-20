# Microsoft Dynamics 365 BC: Update Sales Orders Lines



```
PUT https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-sales-orders-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-sales-orders-lines" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-sales-orders-lines', {
  method: 'PUT',
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
| `companyId` | string | no |  |
| `salesOrderId` | string | no |  |
| `salesOrderLineId` | string | no |  |
| `description` | string | no |  |
| `discountAmount` | number | no |  |
| `discountPercent` | number | no |  |
| `invoiceQuantity` | number | no |  |
| `itemId` | string | no |  |
| `itemVariantId` | string | no |  |
| `lineObjectNumber` | string | no |  |
| `lineType` | string | no |  |
| `locationId` | string | no |  |
| `quantity` | number | no |  |
| `shipmentDate` | string | no |  |
| `shipQuantity` | number | no |  |
| `taxCode` | string | no |  |
| `unitOfMeasureCode` | string | no |  |
| `unitOfMeasureId` | string | no |  |
| `unitPrice` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `PATCH v2.0/companies(:companyId)/salesOrders(:salesOrderId)/salesOrderLines(:salesOrderLineId)` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-orders-lines.md) for the provider-specific parameters and requirements.

