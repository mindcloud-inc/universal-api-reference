# SignalWire: Get SIP Gateway

Retrieves a SIP gateway from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-sip-gateway
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-sip-gateway?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-sip-gateway?${params}`, {
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
| `id` | string | yes | Unique ID of a SIP Gateway. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "id": "string",
      "project_id": "string",
      "sip_gateway": {
        "ciphers": [
          "string"
        ],
        "codecs": [
          "string"
        ],
        "encryption": "string",
        "id": "string",
        "name": "Ava Chen",
        "uri": "string"
      },
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Timestamp when the resource was created. |
| `display_name` | string | Display name of the SIP Gateway. |
| `id` | string | Unique ID of the resource. |
| `project_id` | string | Project ID associated with the resource. |
| `sip_gateway.ciphers` | array<string> | List of supported SIP ciphers. |
| `sip_gateway.codecs` | array<string> | List of supported codecs. |
| `sip_gateway.encryption` | string | Specifies the encryption requirement. |
| `sip_gateway.id` | string | Unique ID of the SIP Gateway. |
| `sip_gateway.name` | string | Display name of the SIP Gateway. |
| `sip_gateway.uri` | string | The URI for the SIP Gateway. |
| `type` | string | Type of the resource. |
| `updated_at` | date | Timestamp when the resource was last updated. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fabric/resources/sip_gateways/{id}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sip-gateway.md) for the provider-specific parameters and requirements.

