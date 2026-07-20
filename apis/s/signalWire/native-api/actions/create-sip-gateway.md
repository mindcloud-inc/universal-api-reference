# Create SIP Gateway with SignalWire

Creates a new SIP gateway in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/sip_gateways`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create SIP Gateway](https://signalwire.com/docs/apis/rest/sip-gateway/create-sip-gateway)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Display name for the SIP Gateway. |
| `uri` | body | `string` | yes | External SIP URI. |
| `encryption` | body | `string` | yes | Specifies the encryption requirement for the SIP connection. |
| `ciphers[]` | body | `array<string>` | yes | List of supported SIP ciphers. |
| `codecs[]` | body | `array<string>` | yes | List of supported codecs for media transmission. |
