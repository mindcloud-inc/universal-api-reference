# Start Extract Job with Hyperbrowser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/extract`
- **Base URL:** `https://api.hyperbrowser.ai`
- **Official documentation:** [Start Extract Job](https://www.hyperbrowser.ai/docs/api-reference/start-an-extract-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes | URLs to extract structured data from. |
| `prompt` | body | `string` | yes | Extraction prompt describing what data to return. |
