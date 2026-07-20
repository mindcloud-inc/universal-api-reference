# List Extractor Variables with WebAutomation.io

Lists variables configured for a specific extractor.

## Endpoint

- **Method:** `GET`
- **Path:** `/extractor_variables/{{EXTRACTOR_ID}}/`
- **Base URL:** `https://webautomation.io/api`
- **Official documentation:** [List Extractor Variables](https://webautomation.io/api/redoc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EXTRACTOR_ID` | path | `number` | yes | The extractor ID. |
