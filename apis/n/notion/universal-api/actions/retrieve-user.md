# Notion: Retrieve User

Retrieves a user from the connected Notion workspace.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-user?connectionId=$CONNECTION_ID&userId=17f3d550-2bf0-49f0-8a2b-8bad283ad83a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "17f3d550-2bf0-49f0-8a2b-8bad283ad83a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-user?${params}`, {
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
| `userId` | string | yes | Identifier of the user to retrieve. Example: `17f3d550-2bf0-49f0-8a2b-8bad283ad83a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
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
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `person` | object |  |
| `requestId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Notion API, this operation is `GET /users/:user_id` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-user.md) for the provider-specific parameters and requirements.

