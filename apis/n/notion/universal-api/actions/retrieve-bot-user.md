# Notion: Retrieve Bot User

Retrieves the current bot user from Notion.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-bot-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-bot-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-bot-user?${params}`, {
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
      "avatarUrl": "https://example.com",
      "bot": {},
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "person": {},
      "requestId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `bot` | object |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `person` | object |  |
| `requestId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Notion API, this operation is `GET /users/me` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-bot-user.md) for the provider-specific parameters and requirements.

