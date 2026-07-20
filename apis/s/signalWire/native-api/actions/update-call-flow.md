# Update Call Flow with SignalWire

Updates an existing call flow in SignalWire.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fabric/resources/call_flows/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update Call Flow](https://signalwire.com/docs/apis/rest/call-flows/update-call-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a Call Flow. |
| `title` | body | `string` | no | The name of the Call Flow |
| `document_version` | body | `number` | no | The current revision of the call flow. Every update must increase this number. |
