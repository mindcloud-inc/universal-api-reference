# Acumatica: Get Inventory Quantity Available



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-inventory-quantity-available
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-inventory-quantity-available" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-inventory-quantity-available', {
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
| `expand` | string | no |  |
| `inventoryID.value` | string | no |  |
| `lastModifiedDateTime.value` | string | no |  |
| `inventoryID` | object | no |  |
| `lastModifiedDateTime` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "InventoryID": {
        "value": "string"
      },
      "LastModifiedDateTime": {
        "value": "string"
      },
      "QtyAvailable": {
        "value": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `InventoryID` | object |  |
| `InventoryID.value` | string |  |
| `LastModifiedDateTime` | object |  |
| `LastModifiedDateTime.value` | string |  |
| `QtyAvailable` | object |  |
| `QtyAvailable.value` | number |  |

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/InventoryQuantityAvailable` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-quantity-available.md) for the provider-specific parameters and requirements.

