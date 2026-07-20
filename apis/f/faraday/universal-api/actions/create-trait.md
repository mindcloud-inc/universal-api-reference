# Faraday: Create Trait

Creates a new user-defined trait in Faraday.

```
POST https://connect.mindcloud.co/v1/universal/faraday/latest/actions/create-trait
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faraday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/create-trait" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/faraday/latest/actions/create-trait', {
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
      "category": "string",
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "literate": "string",
      "name": "Ava Chen",
      "resourceType": "string",
      "statisticalType": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Trait category. |
| `createdAt` | string | Creation timestamp. |
| `description` | string | Trait description. |
| `id` | string | Faraday trait ID. |
| `literate` | string | Trait display name. |
| `name` | string | Trait machine name. |
| `resourceType` | string | Resource type. |
| `statisticalType` | string | Trait statistical type. |
| `status` | string | Trait status. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Faraday API, this operation is `POST /traits` (base URL `https://api.faraday.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-trait.md) for the provider-specific parameters and requirements.

