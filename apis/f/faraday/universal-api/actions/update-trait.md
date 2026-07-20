# Faraday: Update Trait

Updates an existing trait in Faraday.

```
PUT https://connect.mindcloud.co/v1/universal/faraday/latest/actions/update-trait
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faraday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/update-trait" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/faraday/latest/actions/update-trait', {
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
| `trait_id` | string | no | Faraday trait ID. |

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

Through the native Faraday API, this operation is `PATCH /traits/:trait_id` (base URL `https://api.faraday.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-trait.md) for the provider-specific parameters and requirements.

