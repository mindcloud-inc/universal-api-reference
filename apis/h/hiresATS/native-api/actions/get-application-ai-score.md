# Get Application AI Score with 100Hires ATS

Retrieves an application's AI score from 100Hires ATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/:id/ai-score`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Get Application AI Score](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Application ID whose AI score should be returned. |
