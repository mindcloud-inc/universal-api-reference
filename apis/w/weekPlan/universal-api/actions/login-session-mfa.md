# Week Plan: Login Session MFA



```
POST https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/login-session-mfa
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/login-session-mfa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/login-session-mfa', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "AccessToken": "string",
      "RefreshToken": "string",
      "TokenType": "string",
      "UserId": 1,
      "WorkspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccessToken` | string |  |
| `RefreshToken` | string |  |
| `TokenType` | string |  |
| `UserId` | number |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `POST sessions/login-mfa` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login-session-mfa.md) for the provider-specific parameters and requirements.

