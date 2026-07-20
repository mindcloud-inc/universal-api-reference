# Create SIP Endpoint with SignalWire

Creates a new SIP endpoint in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/sip_endpoints`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create SIP Endpoint](https://signalwire.com/docs/apis/rest/sip-credentials/create-sip-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The id of the Sip Endpoint |
| `username` | body | `string` | yes | The username of the Sip Endpoint |
| `caller_id` | body | `string` | yes | The caller ID that will showup when dialing from this Sip Endpoint |
| `send_as` | body | `string` | yes | The Sip username that will show up on the calle's side. Overrides the username. |
| `ciphers[]` | body | `array<string>` | yes | Ciphers that can be enabled for calls on this Sip Endpoint. |
| `codecs[]` | body | `array<string>` | yes | Codecs that can be enabled for calls on this Sip Endpoint. |
| `encryption` | body | `string` | yes | The set encryption type on the Sip Endpoint. |
| `call_handler` | body | `string` | yes | Specify how the SIP endpoint will handle outbound calls. - **default**: The SIP endpoint will pull the outbound policy setting from the [SIP Profile Settings](https://my.signalwire.com?page=sip_profile/edit). This allows centralized management of outbound call behavior across multiple endpoints from a single configuration. - **passthrough**: The SIP endpoint will be allowed to dial PSTN numbers. This permits outbound calling to traditional phone numbers without restrictions. - **block-pstn**: The SIP endpoint will be blocked from dialing PSTN numbers. Use this to restrict the endpoint from initiating calls to the public telephone network. - **resource**: Outbound calls from this SIP endpoint will dial the specified resource and execute its instructions. Requires setting `calling_handler_resource_id` to a valid resource. This enables custom call handling workflows for outbound calls. See the [Fabric REST API](/rest/signalwire-rest/endpoints/fabric) for valid resource types. |
| `calling_handler_resource_id` | body | `string` | yes | If `call_handler` is set to `resource`, this field expects the id of the set resouce. Will be `null` otherwise. |
