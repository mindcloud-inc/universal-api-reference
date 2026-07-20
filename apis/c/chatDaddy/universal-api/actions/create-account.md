# ChatDaddy: Create Account

Creates a new account in ChatDaddy.

```
POST https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Account channel type. Verified live values include `wa`, `messenger`, and `instagram`. |

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

Through the native ChatDaddy API, this operation is `POST /accounts` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

