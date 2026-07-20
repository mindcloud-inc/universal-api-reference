# SignalWire: Create Subscriber Guest Token

Creates a new subscriber guest token in SignalWire.

```
POST https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-subscriber-guest-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-subscriber-guest-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "allowedAddresses[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-subscriber-guest-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "allowedAddresses[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowedAddresses[]` | array<string> | yes | List of up to 10 UUIDs representing the allowed Fabric addresses. |
| `expireAt` | number | no | A unixtime (the number of seconds since 1970-01-01 00:00:00) at which the token should no longer be valid. Defaults to 'two hours from now' |

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
| `refresh_token` | string | Refresh Token |
| `token` | string | Guest Token |

## Native endpoint

Through the native SignalWire API, this operation is `POST /fabric/guests/tokens` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscriber-guest-token.md) for the provider-specific parameters and requirements.

