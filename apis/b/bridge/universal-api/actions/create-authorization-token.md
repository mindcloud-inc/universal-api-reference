# Bridge: Create Authorization Token

Creates a user authorization token in Bridge.

```
POST https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-authorization-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-authorization-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-authorization-token', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userUuid` | string | no | The user UUID |
| `externalUserId` | string | no | Your own user ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "externalUserId": "string",
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string | Authorization token that can be used as authoration bearer token |
| `expiresAt` | date | Expiration date of token |
| `user` | object | A Bridge user represents your user or customer who connects their bank accounts |
| `user.externalUserId` | string | Your own user ID (format: [a-zA-Z0-9-_]{1,128}) |
| `user.uuid` | string | A Universally Unique IDentifier (UUID) as a human-readable string using hexadecimal text with inserted hyphen characters |

## Native endpoint

Through the native Bridge API, this operation is `POST /aggregation/authorization/token` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-authorization-token.md) for the provider-specific parameters and requirements.

