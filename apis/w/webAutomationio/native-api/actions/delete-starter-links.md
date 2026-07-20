# Delete Starter Links with WebAutomation.io

Deletes all starter links from a specific extractor.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/extractors/start_urls/{{EXTRACTOR_ID}}/`
- **Base URL:** `https://webautomation.io/api`
- **Official documentation:** [Delete Starter Links](https://webautomation.io/api/redoc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EXTRACTOR_ID` | path | `number` | yes | The extractor ID. |
