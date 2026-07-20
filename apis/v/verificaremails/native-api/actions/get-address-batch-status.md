# Get Address Batch Status with Verificaremails

Retrieves an address batch validation status from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/address/status/{{requestId}}`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Get Address Batch Status](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Batch request ID returned when the address batch validation was created. |
