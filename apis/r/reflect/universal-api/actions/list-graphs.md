# Reflect: List Graphs

Retrieves graphs from Reflect.

```
GET https://connect.mindcloud.co/v1/universal/reflect/latest/actions/list-graphs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reflect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reflect/latest/actions/list-graphs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reflect/latest/actions/list-graphs?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Reflect API, this operation is `GET /graphs` (base URL `https://reflect.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-graphs.md) for the provider-specific parameters and requirements.

