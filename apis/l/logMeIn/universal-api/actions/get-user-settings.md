# LogMeIn: Get User Settings

Retrieves knowledge base user settings from LogMeIn.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-user-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-user-settings?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "timezone": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | string |  |
| `language` | string |  |
| `name` | string |  |
| `timezone` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `GET /resolve/knowledge-base/v2/user-settings` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-settings.md) for the provider-specific parameters and requirements.

