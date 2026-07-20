# List Extractor Domains with WebAutomation.io

Lists domains configured for a specific extractor.

## Endpoint

- **Method:** `GET`
- **Path:** `/add_extractor_domain/{{EXTRACTOR_ID}}/`
- **Base URL:** `https://webautomation.io/api`
- **Official documentation:** [List Extractor Domains](https://webautomation.io/api/redoc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EXTRACTOR_ID` | path | `number` | yes | The extractor ID. |
