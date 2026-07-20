# SignalWire: Create SIP Endpoint

Creates a new SIP endpoint in SignalWire.

```
POST https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-sip-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-sip-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "username": "Ava Chen",
  "callerId": "string",
  "sendAs": "string",
  "ciphers[]": [
    "string"
  ],
  "codecs[]": [
    "string"
  ],
  "encryption": "string",
  "callHandler": "string",
  "callingHandlerResourceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-sip-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "username": "Ava Chen",
    "callerId": "string",
    "sendAs": "string",
    "ciphers[]": ["string"],
    "codecs[]": ["string"],
    "encryption": "string",
    "callHandler": "string",
    "callingHandlerResourceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the Sip Endpoint |
| `username` | string | yes | The username of the Sip Endpoint |
| `callerId` | string | yes | The caller ID that will showup when dialing from this Sip Endpoint |
| `sendAs` | string | yes | The Sip username that will show up on the calle's side. Overrides the username. |
| `ciphers[]` | array<string> | yes | Ciphers that can be enabled for calls on this Sip Endpoint. |
| `codecs[]` | array<string> | yes | Codecs that can be enabled for calls on this Sip Endpoint. |
| `encryption` | string | yes | The set encryption type on the Sip Endpoint. |
| `callHandler` | string | yes | Specify how the SIP endpoint will handle outbound calls. - **default**: The SIP endpoint will pull the outbound policy setting from the [SIP Profile Settings](https://my.signalwire.com?page=sip_profile/edit). This allows centralized management of outbound call behavior across multiple endpoints from a single configuration. - **passthrough**: The SIP endpoint will be allowed to dial PSTN numbers. This permits outbound calling to traditional phone numbers without restrictions. - **block-pstn**: The SIP endpoint will be blocked from dialing PSTN numbers. Use this to restrict the endpoint from initiating calls to the public telephone network. - **resource**: Outbound calls from this SIP endpoint will dial the specified resource and execute its instructions. Requires setting `calling_handler_resource_id` to a valid resource. This enables custom call handling workflows for outbound calls. See the [Fabric REST API](/rest/signalwire-rest/endpoints/fabric) for valid resource types. |
| `callingHandlerResourceId` | string | yes | If `call_handler` is set to `resource`, this field expects the id of the set resouce. Will be `null` otherwise. |

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
      "sip_endpoint": {
        "call_handler": "string",
        "caller_id": "string",
        "calling_handler_resource_id": "string",
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
| `created_at` | date | Date and time when the resource was created. |
| `display_name` | string | Display name of the SIP Endpoint Fabric Resource |
| `id` | string | Unique ID of the SIP Endpoint. |
| `project_id` | string | Unique ID of the Project. |
| `sip_endpoint.call_handler` | string | Specify how the SIP endpoint will handle outbound calls. - **default**: The SIP endpoint will pull the outbound policy setting from the [SIP Profile Settings](https://my.signalwire.com?page=sip_profile/edit). This allows centralized management of outbound call behavior across multiple endpoints from a single configuration. - **passthrough**: The SIP endpoint will be allowed to dial PSTN numbers. This permits outbound calling to traditional phone numbers without restrictions. - **block-pstn**: The SIP endpoint will be blocked from dialing PSTN numbers. Use this to restrict the endpoint from initiating calls to the public telephone network. - **resource**: Outbound calls from this SIP endpoint will dial the specified resource and execute its instructions. Requires setting `calling_handler_resource_id` to a valid resource. This enables custom call handling workflows for outbound calls. See the [Fabric REST API](/rest/signalwire-rest/endpoints/fabric) for valid resource types. |
| `sip_endpoint.caller_id` | string | The caller ID that will showup when dialing from this Sip Endpoint |
| `sip_endpoint.calling_handler_resource_id` | string | If `call_handler` is set to `resource`, this field expects the id of the set resouce. Will be `null` otherwise. |
| `sip_endpoint.ciphers` | array<string> | Ciphers that can be enabled for calls on this Sip Endpoint. |
| `sip_endpoint.codecs` | array<string> | Codecs that can be enabled for calls on this Sip Endpoint. |
| `sip_endpoint.encryption` | string | The set encryption type on the Sip Endpoint. |
| `sip_endpoint.id` | string | The id of the Sip Endpoint |
| `sip_endpoint.send_as` | string | The Sip username that will show up on the calle's side. Overrides the username. |
| `sip_endpoint.username` | string | The username of the Sip Endpoint |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /fabric/resources/sip_endpoints` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sip-endpoint.md) for the provider-specific parameters and requirements.

