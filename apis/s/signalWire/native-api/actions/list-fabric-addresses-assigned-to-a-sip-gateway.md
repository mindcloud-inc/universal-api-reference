# List Fabric Addresses assigned to a SIP Gateway with SignalWire

Retrieves Fabric addresses assigned to a SIP gateway from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/sip_gateways/resources/sip_gateways/{resource_id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List Fabric Addresses assigned to a SIP Gateway](https://signalwire.com/docs/apis/rest/sip-gateway/list-sip-gateway-addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource_id` | path | `string` | yes | The unique identifier of the SIP Gateway. |
