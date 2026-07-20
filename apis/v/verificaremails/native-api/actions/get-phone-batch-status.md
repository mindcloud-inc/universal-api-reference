# Get Phone Batch Status with Verificaremails

Retrieves a phone batch validation status from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/phone/status/{{requestId}}`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Get Phone Batch Status](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Batch request ID returned when the phone batch validation was created. |
