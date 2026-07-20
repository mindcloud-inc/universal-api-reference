# List SWML Script Addresses with SignalWire

Retrieves SWML script addresses from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/swml_scripts/{id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List SWML Script Addresses](https://signalwire.com/docs/apis/rest/swml-scripts/list-swml-script-addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the SWML Script. |
