# Get All Active Models From List with SectorFlow.AI

## Endpoint

- **Method:** `POST`
- **Path:** `/models/list/all`
- **Base URL:** `https://platform.sectorflow.ai/api/v1`
- **Official documentation:** [Get All Active Models From List](https://docs.sectorflowai.com/reference/models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelIds[]` | body | `array<string>` | yes | List of model UUIDs. |
