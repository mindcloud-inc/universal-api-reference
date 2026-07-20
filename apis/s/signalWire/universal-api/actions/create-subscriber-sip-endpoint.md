# SignalWire: Create Subscriber SIP Endpoint

Creates a new subscriber SIP endpoint in SignalWire.

```
POST https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-subscriber-sip-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-subscriber-sip-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fabricSubscriberId": "string",
  "username": "Ava Chen",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-subscriber-sip-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fabricSubscriberId": "string",
    "username": "Ava Chen",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fabricSubscriberId` | string | yes | Unique ID of a Fabric Subscriber. |
| `username` | string | yes | Username of the Sip Endpoint. |
| `password` | string | yes | Password of the Sip Endpoint. |
| `callerId` | string | no | Caller ID of the Sip Endpoint. |
| `sendAs` | string | no | The Number to send as. |
| `ciphers[]` | array<string> | no | Ciphers of the Sip Endpoint. |
| `codecs[]` | array<string> | no | Codecs of the Sip Endpoint. |
| `encryption` | string | no | Encryption requirement of the Sip Endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "caller_id": "string",
      "ciphers": [
        "string"
      ],
      "codecs": [
        "string"
      ],
      "encryption": "string",
      "id": "string",
      "send_as": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caller_id` | string | Caller ID of the Sip Endpoint. |
| `ciphers` | array<string> | Ciphers of the Sip Endpoint. |
| `codecs` | array<string> | Codecs of the Sip Endpoint. |
| `encryption` | string | Encryption requirement of the Sip Endpoint. |
| `id` | string | Unique ID of the Sip Endpoint. |
| `send_as` | string | Purchased or verified number |
| `username` | string | Username of the Sip Endpoint. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscriber-sip-endpoint.md) for the provider-specific parameters and requirements.

