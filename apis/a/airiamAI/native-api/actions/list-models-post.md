# List Models With Body with Airiam AI

Retrieves active models from Airiam AI by model IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/models/list`
- **Base URL:** `https://platform.sectorflow.ai`
- **Official documentation:** [List Models With Body](https://docs.ai.airiam.com/reference/models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseModels[]` | body | `array<string>` | yes | Base model identifiers to include. |
