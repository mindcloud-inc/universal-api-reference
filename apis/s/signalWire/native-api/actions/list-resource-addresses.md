# List Resource Addresses with SignalWire

Retrieves resource addresses from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/{id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List Resource Addresses](https://signalwire.com/docs/apis/rest/addresses/list-resource-addresses-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the Resource. |
