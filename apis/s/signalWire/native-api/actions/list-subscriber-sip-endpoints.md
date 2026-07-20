# List Subscriber SIP Endpoints with SignalWire

Retrieves subscriber SIP endpoints from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List Subscriber SIP Endpoints](https://signalwire.com/docs/apis/rest/subscribers/sip-credentials/list-subscriber-sip-credentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fabric_subscriber_id` | path | `string` | yes | Unique ID of a Fabric Subscriber. |
