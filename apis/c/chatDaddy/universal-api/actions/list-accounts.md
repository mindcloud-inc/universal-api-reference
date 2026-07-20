# ChatDaddy: List Accounts

Retrieves connected account records from ChatDaddy.

```
GET https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-accounts?${params}`, {
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
      "accountId": "string",
      "createdAt": "string",
      "createdBy": "string",
      "nickname": "Ava Chen",
      "ownerId": "string",
      "settings": {},
      "state": "string",
      "stateInfo": {},
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Account identifier. |
| `createdAt` | string | ISO timestamp when the account was created. |
| `createdBy` | string | User identifier that created the account. |
| `nickname` | string | Account nickname. |
| `ownerId` | string | Workspace owner identifier. |
| `settings` | object | Connection settings for the account. |
| `state` | string | Current connection state. |
| `stateInfo` | object | Additional state metadata. |
| `type` | string | Channel type for the account. |
| `updatedAt` | string | ISO timestamp when the account was last updated. |

## Native endpoint

Through the native ChatDaddy API, this operation is `GET /accounts` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

