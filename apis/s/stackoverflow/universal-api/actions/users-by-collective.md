# Stackoverflow: List Collective Users

Retrieves users for collectives from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/users-by-collective
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/users-by-collective?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/users-by-collective?${params}`, {
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
      "display_name": "Ava Chen",
      "link": "https://example.com",
      "reputation": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `display_name` | string |  |
| `link` | string |  |
| `reputation` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /collectives/[:slugs]/users` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/users-by-collective.md) for the provider-specific parameters and requirements.

