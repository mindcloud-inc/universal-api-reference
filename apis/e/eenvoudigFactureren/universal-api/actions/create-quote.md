# EenvoudigFactureren: Create Quote

Creates a new quote in EenvoudigFactureren.

```
POST https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/create-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EenvoudigFactureren `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/create-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/create-quote', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "client_name": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "number": "string",
      "quote_id": 1,
      "status": "string",
      "total": 1,
      "uri": "string",
      "valid_until": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_name` | string |  |
| `date` | date |  |
| `number` | string |  |
| `quote_id` | number |  |
| `status` | string |  |
| `total` | number |  |
| `uri` | string |  |
| `valid_until` | date |  |

## Native endpoint

Through the native EenvoudigFactureren API, this operation is `POST /quotes` (base URL `https://eenvoudigfactureren.be/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quote.md) for the provider-specific parameters and requirements.

