# Get Subscriber SIP Endpoint with SignalWire

Retrieves a subscriber SIP endpoint from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Get Subscriber SIP Endpoint](https://signalwire.com/docs/apis/rest/subscribers/sip-credentials/get-subscriber-sip-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a Sip Endpoint. |
| `fabric_subscriber_id` | path | `string` | yes | Unique ID of a Fabric Subscriber. |
