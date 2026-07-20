# Port API AI: List Migrations

Retrieves migrations from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/list-migrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/list-migrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/list-migrations?${params}`, {
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
      "migrations": [
        {}
      ],
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `migrations` | array<object> |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `GET /migrations` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-migrations.md) for the provider-specific parameters and requirements.

