# Acumatica: Create/Update Sales Orders



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-update-sales-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-update-sales-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-update-sales-orders', {
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
| `OrderNbr` | object | no |  |
| `OrderType` | object | no |  |
| `CustomerID.value` | string | no |  |
| `customerOrder.value` | string | no |  |
| `Description.value` | string | no |  |
| `ExternalRef` | object | no |  |
| `ExternalRef.value` | string | no |  |
| `Hold.value` | string | no |  |
| `lastModified.value` | string | no |  |
| `OrderNbr.value` | string | no |  |
| `OrderType.value` | string | no |  |
| `preferredWarehouseID.value` | string | no |  |
| `requestedOn.value` | string | no |  |
| `Status.value` | string | no |  |
| `UsrLogShipID.value` | string | no |  |
| `UsrLogSyncDateTime.value` | string | no |  |
| `CustomerID` | object | no |  |
| `Status` | object | no |  |
| `Description` | object | no |  |
| `Hold` | object | no |  |
| `requestedOn` | object | no |  |
| `UsrLogShipID` | object | no |  |
| `preferredWarehouseID` | object | no |  |
| `customerOrder` | object | no |  |
| `UsrLogSyncDateTime` | object | no |  |
| `lastModified` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumatica API returns.

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-update-sales-orders.md) for the provider-specific parameters and requirements.

