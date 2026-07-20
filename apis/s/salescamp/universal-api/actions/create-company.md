# Salescamp: Create Company



```
POST https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salescamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Company name |
| `email` | string | no | Company email |
| `phone` | string | no | Company phone |
| `website` | string | no | Company website |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Salescamp API, this operation is `POST /v1/collections/69cd24c2f24a3ccfd974811e/items` (base URL `https://api.salescamp.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

