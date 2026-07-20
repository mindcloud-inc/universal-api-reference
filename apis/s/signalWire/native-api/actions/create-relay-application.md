# Create Relay Application with SignalWire

Creates a new relay application in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/relay_applications`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create Relay Application](https://signalwire.com/docs/apis/rest/relay-application/create-relay-application)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the Relay Application |
| `topic` | body | `string` | yes | Topic of the Relay Application |
| `call_status_callback_url` | body | `string` | no | Call status callback URL |
