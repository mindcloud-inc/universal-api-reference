# Create FreeSWITCH Connector with SignalWire

Creates a new FreeSWITCH connector in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/freeswitch_connectors`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create FreeSWITCH Connector](https://signalwire.com/docs/apis/rest/freeswitch-connector/create-freeswitch-connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the FreeSWITCH Connector |
| `token` | body | `string` | yes | FreeSWITCH token |
