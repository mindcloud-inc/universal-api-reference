# Realcrux: List Mail Lists



```
GET https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/list-mail-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Realcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/list-mail-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/list-mail-lists?${params}`, {
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
      "data": [
        {}
      ],
      "pagination": {},
      "permissions": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Mail lists returned by the authenticated Realcrux account. |
| `pagination` | object | Pagination metadata for the list collection. |
| `permissions` | object | Provider permission envelope for the list response; may be null. |

## Native endpoint

Through the native Realcrux API, this operation is `GET lists` (base URL `https://sendcrux.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mail-lists.md) for the provider-specific parameters and requirements.

