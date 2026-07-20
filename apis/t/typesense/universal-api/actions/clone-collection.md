# Typesense: Clone Collection

Creates a collection by cloning another in Typesense.

```
POST https://connect.mindcloud.co/v1/universal/typesense/latest/actions/clone-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/clone-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typesense/latest/actions/clone-collection', {
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
      "fields": [
        {}
      ],
      "name": "Ava Chen",
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> |  |
| `name` | string |  |
| `response` | object |  |

## Native endpoint

Through the native Typesense API, this operation is `POST /collections` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clone-collection.md) for the provider-specific parameters and requirements.

