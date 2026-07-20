# Get Phone Syntactic Batch Status with Verificaremails

Retrieves a phone syntactic batch validation status from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/phonesyntactic/status/{{requestId}}`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Get Phone Syntactic Batch Status](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Batch request ID returned when the phone syntactic batch validation was created. |
