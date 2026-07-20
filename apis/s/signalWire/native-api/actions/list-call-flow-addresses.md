# List Call Flow Addresses with SignalWire

Retrieves call flow addresses from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/call_flow/{id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List Call Flow Addresses](https://signalwire.com/docs/apis/rest/call-flows/list-call-flow-addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the Call Flow. |
