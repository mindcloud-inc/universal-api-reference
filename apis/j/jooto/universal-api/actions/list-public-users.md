# Jooto: List Public Users

Retrieves a list of public users from Jooto.

```
GET https://connect.mindcloud.co/v1/universal/jooto/latest/actions/list-public-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jooto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jooto/latest/actions/list-public-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jooto/latest/actions/list-public-users?${params}`, {
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
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Unique identifier for the user. |

## Native endpoint

Through the native Jooto API, this operation is `GET /api/public/v1/users` (base URL `https://app.jooto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-users.md) for the provider-specific parameters and requirements.

