# Update Subscriber SIP Endpoint with SignalWire

Updates an existing subscriber SIP endpoint in SignalWire.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update Subscriber SIP Endpoint](https://signalwire.com/docs/apis/rest/subscribers/sip-credentials/update-subscriber-sip-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a Sip Endpoint. |
| `fabric_subscriber_id` | path | `string` | yes | Unique ID of a Fabric Subscriber. |
| `username` | body | `string` | no | Username of the Sip Endpoint. |
| `password` | body | `string` | no | Password of the Sip Endpoint. |
| `caller_id` | body | `string` | no | Caller ID of the Sip Endpoint. |
| `send_as` | body | `string` | no | The Number to send as. |
| `ciphers[]` | body | `array<string>` | no | Ciphers of the Sip Endpoint. |
| `codecs[]` | body | `array<string>` | no | Codecs of the Sip Endpoint. |
| `encryption` | body | `string` | no | Encryption requirement of the Sip Endpoint. |
