# Get Name Batch Status with Verificaremails

Retrieves a name batch validation status from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/name/status/{{requestId}}`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Get Name Batch Status](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Batch request ID returned when the name batch validation was created. |
