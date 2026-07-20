# Faraday: List Traits

Retrieves a list of traits from Faraday.

```
GET https://connect.mindcloud.co/v1/universal/faraday/latest/actions/list-traits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faraday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/list-traits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faraday/latest/actions/list-traits?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Faraday API, this operation is `GET /traits` (base URL `https://api.faraday.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-traits.md) for the provider-specific parameters and requirements.

