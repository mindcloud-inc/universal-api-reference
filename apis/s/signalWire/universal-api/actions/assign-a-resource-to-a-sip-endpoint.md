# SignalWire: Assign a Resource to a SIP endpoint

Assigns a resource to a SIP endpoint in SignalWire.

```
PUT https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/assign-a-resource-to-a-sip-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/assign-a-resource-to-a-sip-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "sipEndpointId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/assign-a-resource-to-a-sip-endpoint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "sipEndpointId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique identifier of the Resource. |
| `sipEndpointId` | string | yes | The unique identifier of the SIP endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": {
        "audio": "string"
      },
      "cover_url": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "preview_url": "https://example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels.audio` | string | Audio Channel of Fabric Address |
| `cover_url` | string | The cover URL for the SIP endpoint. |
| `id` | string | The unique identifier of the SIP endpoint. |
| `name` | string | The name for the SIP endpoint. |
| `preview_url` | string | The preview URL for the SIP endpoint. |
| `type` | string | The Resource type |

## Native endpoint

Through the native SignalWire API, this operation is `POST /fabric/resources/sip_endpoints/resources/{id}/sip_endpoints` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-a-resource-to-a-sip-endpoint.md) for the provider-specific parameters and requirements.

