# Simplesat: Bulk Upsert Customers

Creates or updates multiple customers in Simplesat.

```
POST https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/bulk-upsert-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/bulk-upsert-customers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/bulk-upsert-customers', {
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
| `customers[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detail": "string",
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detail` | string |  |
| `request_id` | string |  |

## Native endpoint

Through the native Simplesat API, this operation is `POST /api/v1/customers/bulk` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-upsert-customers.md) for the provider-specific parameters and requirements.

