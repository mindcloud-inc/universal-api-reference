# Get Email Batch Status with Verificaremails

Retrieves an email batch validation status from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/email/status/{{requestId}}`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Get Email Batch Status](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Batch request ID returned when the email batch validation was created. |
