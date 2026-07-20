# List SIP Endpoint Addresses with SignalWire

Retrieves SIP endpoint addresses from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/sip_endpoints/{id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List SIP Endpoint Addresses](https://signalwire.com/docs/apis/rest/sip-credentials/list-sip-credential-addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the SIP Endpoint. |
