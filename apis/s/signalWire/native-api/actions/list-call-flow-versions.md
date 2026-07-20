# List Call Flow Versions with SignalWire

Retrieves call flow versions from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/call_flow/{id}/versions`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List Call Flow Versions](https://signalwire.com/docs/apis/rest/call-flows/list-call-flow-versions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the Call Flow. |
