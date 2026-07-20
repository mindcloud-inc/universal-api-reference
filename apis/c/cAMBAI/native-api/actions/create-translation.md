# Create Translation with CAMB.AI

Creates a new translation task in CAMB.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/translate`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Create Translation](https://docs.camb.ai/api-reference/endpoint/create-translation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_language` | body | `number` | yes | Source language identifier from Get Source Languages. |
| `target_language` | body | `number` | yes | Target language identifier from Get Target Languages. |
| `texts[]` | body | `array<string>` | yes | One or more text segments to translate. |
