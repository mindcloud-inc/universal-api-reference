# Acumatica: Send Inventory Quantity(to Custom Field)



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/send-inventory-quantityto-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/send-inventory-quantityto-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/send-inventory-quantityto-custom-field', {
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
| `UsrLogSyncDateTime.value` | string | no |  |
| `InventoryID.value` | string | no |  |
| `UsrLogQOH` | object | no |  |
| `UsrLogQOH.value` | number | no |  |
| `WarehouseID.value` | string | no |  |
| `InventoryID` | object | no |  |
| `WarehouseID` | object | no |  |
| `UsrLogSyncDateTime` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumatica API returns.

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/ItemWarehouse` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-inventory-quantityto-custom-field.md) for the provider-specific parameters and requirements.

