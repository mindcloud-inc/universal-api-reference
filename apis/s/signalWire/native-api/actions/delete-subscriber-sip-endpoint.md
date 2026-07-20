# Delete Subscriber SIP Endpoint with SignalWire

Deletes an existing subscriber SIP endpoint from SignalWire.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Delete Subscriber SIP Endpoint](https://signalwire.com/docs/apis/rest/subscribers/sip-credentials/delete-subscriber-sip-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a Sip Endpoint. |
| `fabric_subscriber_id` | path | `string` | yes | Unique ID of a Fabric Subscriber. |
