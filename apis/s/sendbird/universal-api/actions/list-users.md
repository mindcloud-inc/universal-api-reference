# Sendbird: List Users



```
GET https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendbird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-users?${params}`, {
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
| `limit` | number | no | Number of users to return per page. Acceptable values are 1 to 100. |
| `activeMode` | string | no | Activation status filter: activated, deactivated, or all. |
| `showBot` | boolean | no | Include bots in the result set. |
| `nickname` | string | no | Exact nickname filter. |
| `nicknameStartsWith` | string | no | Prefix filter for nicknames. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `token` | string | no | Page token indicating the starting index of results to retrieve. |
| `userIds` | string | no | Comma-separated urlencoded user IDs to include. |
| `metadataKey` | string | no | Metadata key to filter on when paired with metadata values. |
| `metadataValuesIn` | string | no | Comma-separated metadata values used with Metadata Key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "isActive": true,
      "nickname": "Ava Chen",
      "profileUrl": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `isActive` | boolean |  |
| `nickname` | string |  |
| `profileUrl` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Sendbird API, this operation is `GET /users` (base URL `https://api-{{credentials.applicationId}}.sendbird.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

