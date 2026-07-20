# Returnless: Add Return Order Note

Adds a note to a return order in Returnless.

```
PUT https://connect.mindcloud.co/v1/universal/returnless/latest/actions/add-return-order-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Returnless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/returnless/latest/actions/add-return-order-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "returnOrder": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/returnless/latest/actions/add-return-order-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "returnOrder": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `returnOrder` | string | yes | The unique identifier of the return order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Return order object produced by this mutation. |
| `meta` | object | Execution metadata. |

## Native endpoint

Through the native Returnless API, this operation is `POST /2025-01/return-orders/{returnOrder}/notes` (base URL `https://api-v2.returnless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-return-order-note.md) for the provider-specific parameters and requirements.

