# SignalWire: Refresh Subscriber Token

Refreshes a subscriber token in SignalWire.

```
POST https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/refresh-subscriber-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/refresh-subscriber-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "refreshToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/refresh-subscriber-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "refreshToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `refreshToken` | string | yes | The refresh token previously issued alongside a subscriber access token. This token is used to request a new access token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "refresh_token": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `refresh_token` | string | A new refresh token, valid for 2 hours and 5 minutes. |
| `token` | string | A newly generated subscriber access token, valid for 2 hours. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /fabric/subscribers/tokens/refresh` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-subscriber-token.md) for the provider-specific parameters and requirements.

