# Update SIP Endpoint with SignalWire

Updates an existing SIP endpoint in SignalWire.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fabric/resources/sip_endpoints/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update SIP Endpoint](https://signalwire.com/docs/apis/rest/sip-credentials/update-sip-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a SIP Endpoint. |
| `username` | body | `string` | no | The username of the Sip Endpoint |
| `caller_id` | body | `string` | no | The caller ID that will showup when dialing from this Sip Endpoint |
| `send_as` | body | `string` | no | The Sip username that will show up on the calle's side. Overrides the username. |
| `ciphers[]` | body | `array<string>` | no | Ciphers that can be enabled for calls on this Sip Endpoint. |
| `codecs[]` | body | `array<string>` | no | Codecs that can be enabled for calls on this Sip Endpoint. |
| `encryption` | body | `string` | no | The set encryption type on the Sip Endpoint. |
| `call_handler` | body | `string` | no | Specify how the SIP endpoint will handle outbound calls. - **default**: The SIP endpoint will pull the outbound policy setting from the [SIP Profile Settings](https://my.signalwire.com?page=sip_profile/edit). This allows centralized management of outbound call behavior across multiple endpoints from a single configuration. - **passthrough**: The SIP endpoint will be allowed to dial PSTN numbers. This permits outbound calling to traditional phone numbers without restrictions. - **block-pstn**: The SIP endpoint will be blocked from dialing PSTN numbers. Use this to restrict the endpoint from initiating calls to the public telephone network. - **resource**: Outbound calls from this SIP endpoint will dial the specified resource and execute its instructions. Requires setting `calling_handler_resource_id` to a valid resource. This enables custom call handling workflows for outbound calls. See the [Fabric REST API](/rest/signalwire-rest/endpoints/fabric) for valid resource types. |
| `calling_handler_resource_id` | body | `string` | yes | If `call_handler` is set to `resource`, this field will contain the id of the set resouce. Will be `null` otherwise. |
