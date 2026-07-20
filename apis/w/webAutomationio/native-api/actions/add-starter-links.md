# Add Starter Links with WebAutomation.io

Replaces an extractor's starter links with a new list.

## Endpoint

- **Method:** `POST`
- **Path:** `/extractors/start_urls/{{EXTRACTOR_ID}}/`
- **Base URL:** `https://webautomation.io/api`
- **Official documentation:** [Add Starter Links](https://webautomation.io/api/redoc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EXTRACTOR_ID` | path | `number` | yes | The extractor ID. |
| `start_urls[]` | body | `array<string>` | yes | The list of start URLs to set on the extractor. |
