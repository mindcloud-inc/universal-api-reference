# SignalWire: List Subscriber SIP Endpoints

Retrieves subscriber SIP endpoints from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-subscriber-sip-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-subscriber-sip-endpoints?connectionId=$CONNECTION_ID&fabricSubscriberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fabricSubscriberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-subscriber-sip-endpoints?${params}`, {
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
| `fabricSubscriberId` | string | yes | Unique ID of a Fabric Subscriber. |

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

Through the native SignalWire API, this operation is `GET /fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriber-sip-endpoints.md) for the provider-specific parameters and requirements.

