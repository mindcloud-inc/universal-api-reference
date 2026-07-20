# Update FreeSWITCH Connector with SignalWire

Updates an existing FreeSWITCH connector in SignalWire.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fabric/resources/freeswitch_connectors/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update FreeSWITCH Connector](https://signalwire.com/docs/apis/rest/freeswitch-connector/update-freeswitch-connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a FreeSWITCH Connector. |
| `name` | body | `string` | no | Name of the FreeSWITCH Connector |
| `caller_id` | body | `string` | no | Caller ID for the connector |
| `send_as` | body | `string` | no | Send as identifier |
