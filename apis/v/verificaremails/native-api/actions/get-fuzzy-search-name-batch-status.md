# Get Fuzzy Search Name Batch Status with Verificaremails

Retrieves a fuzzy search name batch validation status from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/fuzzysearch/status/{{requestId}}`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Get Fuzzy Search Name Batch Status](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Batch request ID returned when the fuzzy search name batch validation was created. |
