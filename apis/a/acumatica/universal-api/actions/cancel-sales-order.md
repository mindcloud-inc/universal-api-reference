# Acumatica: Cancel Sales Order



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/cancel-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/cancel-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entity.OrderType.value": "string",
  "entity.OrderNbr.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/cancel-sales-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entity.OrderType.value": "string",
    "entity.OrderNbr.value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entity` | object | no |  |
| `entity.OrderType` | object | no |  |
| `entity.OrderType.value` | string | yes |  |
| `entity.OrderNbr` | object | no |  |
| `entity.OrderNbr.value` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether Acumatica accepted the operation. |

## Native endpoint

Through the native Acumatica API, this operation is `POST /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder/CancelSalesOrder` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-sales-order.md) for the provider-specific parameters and requirements.

