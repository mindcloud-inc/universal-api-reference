# Assign a Resource to a SIP endpoint with SignalWire

Assigns a resource to a SIP endpoint in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/sip_endpoints/resources/{id}/sip_endpoints`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Assign a Resource to a SIP endpoint](https://signalwire.com/docs/apis/rest/sip-credentials/assign-resource-to-sip-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the Resource. |
| `sip_endpoint_id` | body | `string` | yes | The unique identifier of the SIP endpoint. |
