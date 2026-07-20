# Get Study Material with WaniKani

Retrieves a study material from WaniKani.

## Endpoint

- **Method:** `GET`
- **Path:** `/study_materials/[:id]`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [Get Study Material](https://docs.api.wanikani.com/20170710/#get-a-specific-study-material)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique identifier of the study material. |
