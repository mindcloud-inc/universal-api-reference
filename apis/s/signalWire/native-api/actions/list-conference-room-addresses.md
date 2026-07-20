# List Conference Room Addresses with SignalWire

Retrieves conference room addresses from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/conference_room/{id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List Conference Room Addresses](https://signalwire.com/docs/apis/rest/conference-rooms/list-conference-room-addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the Conference Room. |
