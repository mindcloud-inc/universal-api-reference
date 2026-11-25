# Celigo: Get Token Info



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-token-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-token-info?${params}`, {
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
      "byUser": {
        "accessLevel": "string",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "environment": {
        "envUserId": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "ownerUser": {
        "company": "string",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "token": {
        "autoPurgeAt": "2026-05-07T12:00:00.000Z",
        "fullAccess": true,
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `byUser.accessLevel` | string | Acting user's account-wide access level, such as owner. |
| `byUser.email` | string | Email of the acting user. |
| `byUser.id` | string | ID of the user acting through the token. |
| `byUser.name` | string | Name of the acting user. |
| `environment.envUserId` | string | User record that owns this environment's resources. |
| `environment.id` | string | Environment ID. |
| `environment.name` | string | Environment the token is bound to, such as Production or Sandbox. |
| `ownerUser.company` | string | Company name on the owner's profile. |
| `ownerUser.email` | string | Account owner's email. |
| `ownerUser.id` | string | Account owner's user ID, which identifies the account. |
| `ownerUser.name` | string | Account owner's name. |
| `token.autoPurgeAt` | date | When the token is automatically deleted, if set. |
| `token.fullAccess` | boolean | True for Full access service tokens; false for Custom-scope tokens. |
| `token.id` | string | ID of the access token record. |
| `token.name` | string | Display name of the token. |
| `token.type` | string | Credential kind: service, personal, or agent. |
| `userId` | string | User record the token is bound to (the account owner for Production tokens). |

## Native endpoint

Through the native Celigo API, this operation is `GET /tokenInfo` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-info.md) for the provider-specific parameters and requirements.

