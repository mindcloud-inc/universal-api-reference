# List FreeSWITCH Connector Addresses with SignalWire

Retrieves FreeSWITCH connector addresses from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/freeswitch_connectors/{id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List FreeSWITCH Connector Addresses](https://signalwire.com/docs/apis/rest/freeswitch-connector/list-freeswitch-connector-addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the FreeSWITCH Connector. |
