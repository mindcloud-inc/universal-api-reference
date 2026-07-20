# Hex: Get Collection



```
GET https://connect.mindcloud.co/v1/universal/hex/latest/actions/get-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hex/latest/actions/get-collection?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hex/latest/actions/get-collection?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Unique ID for a collection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creator": {
        "email": "ava@example.com",
        "id": "string"
      },
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "sharing": {
        "groups": [
          {}
        ],
        "users": [
          {}
        ],
        "workspace": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator.email` | string |  |
| `creator.id` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `sharing.groups` | array<object> |  |
| `sharing.users` | array<object> |  |
| `sharing.workspace` | object |  |

## Native endpoint

Through the native Hex API, this operation is `GET /collections/{collectionId}` (base URL `https://app.hex.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection.md) for the provider-specific parameters and requirements.

