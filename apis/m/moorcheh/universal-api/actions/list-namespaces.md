# Moorcheh: List Namespaces

Retrieves all namespaces in your Moorcheh account.

```
GET https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/list-namespaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/list-namespaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/list-namespaces?${params}`, {
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
      "namespaces": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "item_count": 1,
          "namespace_name": "Ava Chen",
          "type": "Ava Chen",
          "vector_dimension": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `namespaces` | array<object> | Namespaces returned for the authenticated Moorcheh account. |
| `namespaces[].created_at` | date | Namespace creation timestamp. |
| `namespaces[].item_count` | number | Total item count in the namespace. |
| `namespaces[].namespace_name` | string | Unique namespace name. |
| `namespaces[].type` | string | Namespace type, either text or vector. |
| `namespaces[].vector_dimension` | number | Vector dimension, or null for text namespaces. |

## Native endpoint

Through the native Moorcheh API, this operation is `GET /namespaces` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-namespaces.md) for the provider-specific parameters and requirements.

