# Update SIP Gateway with SignalWire

Updates an existing SIP gateway in SignalWire.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/fabric/resources/sip_gateways/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update SIP Gateway](https://signalwire.com/docs/apis/rest/sip-gateway/update-sip-gateway)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a SIP Gateway. |
| `name` | body | `string` | no | Display name for the SIP Gateway. |
| `uri` | body | `string` | no | External SIP URI. |
| `encryption` | body | `string` | no | Specifies the encryption requirement for the SIP connection. |
| `ciphers[]` | body | `array<string>` | no | List of supported SIP ciphers. |
| `codecs[]` | body | `array<string>` | no | List of supported codecs for media transmission. |
