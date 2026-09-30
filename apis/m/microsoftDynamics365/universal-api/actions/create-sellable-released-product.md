# Microsoft Dynamics 365: Create Sellable Released Product



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-sellable-released-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-sellable-released-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-sellable-released-product', {
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
| `dataAreaId` | string | no |  |
| `FieldServiceProductType` | string | no |  |
| `InventoryUnitDecimalPrecision` | number | no |  |
| `IsSalesStopped` | string | no |  |
| `IsStockedProduct` | string | no |  |
| `ProductDescription` | string | no |  |
| `ProductName` | string | no |  |
| `ProductNumber` | string | no |  |
| `ProductType` | string | no |  |
| `SalesPrice` | number | no |  |
| `SalesUnitDecimalPrecision` | number | no |  |
| `SalesUnitSymbol` | string | no | Ea / Pc |
| `UnitCost` | number | no |  |
| `CurrencyCode` | string | no |  |
| `InventoryUnitSymbol` | string | no | Ea / Pc |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `POST SellableReleasedProducts` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sellable-released-product.md) for the provider-specific parameters and requirements.

