# DateX: Update Sales Order Lines



```
PUT https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/update-sales-order-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/update-sales-order-lines" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderLines[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/update-sales-order-lines', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderLines[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderLines[]` | array<object> | yes | Array of sales order line objects to update, matching the documented order_lines schema. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |

## Native endpoint

Through the native DateX API, this operation is `POST sales_order_lines/update` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-order-lines.md) for the provider-specific parameters and requirements.

