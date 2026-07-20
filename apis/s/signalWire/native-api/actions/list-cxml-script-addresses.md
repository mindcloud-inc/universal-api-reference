# List cXML Script Addresses with SignalWire

Retrieves cXML script addresses from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/cxml_scripts/{id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List cXML Script Addresses](https://signalwire.com/docs/apis/rest/cxml-scripts/list-cxml-script-addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the cXML Script. |
