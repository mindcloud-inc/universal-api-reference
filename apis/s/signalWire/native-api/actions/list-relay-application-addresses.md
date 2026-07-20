# List Relay Application Addresses with SignalWire

Retrieves relay application addresses from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/relay_applications/{id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List Relay Application Addresses](https://signalwire.com/docs/apis/rest/relay-application/list-relay-application-addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the Relay Application. |
