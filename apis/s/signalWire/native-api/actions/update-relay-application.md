# Update Relay Application with SignalWire

Updates an existing relay application in SignalWire.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fabric/resources/relay_applications/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update Relay Application](https://signalwire.com/docs/apis/rest/relay-application/update-relay-application)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a Relay Application. |
| `name` | body | `string` | no | Name of the Relay Application |
| `topic` | body | `string` | no | Topic of the Relay Application |
| `call_status_callback_url` | body | `string` | no | Call status callback URL |
