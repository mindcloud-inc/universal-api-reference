# Rownd Data Privacy: Revoke User Sessions



```
PUT https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/revoke-user-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/revoke-user-sessions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/revoke-user-sessions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user` | string | yes | Rownd user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "revoked": true,
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `revoked` | boolean | Whether user sessions were revoked. |
| `user_id` | string | Rownd user identifier. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `POST /users/:user/signout` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-user-sessions.md) for the provider-specific parameters and requirements.

