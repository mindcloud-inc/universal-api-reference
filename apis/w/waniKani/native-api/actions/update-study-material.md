# Update Study Material with WaniKani

Updates an existing study material in WaniKani.

## Endpoint

- **Method:** `PUT`
- **Path:** `/study_materials/[:id]`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [Update Study Material](https://docs.api.wanikani.com/20170710/#update-a-study-material)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique identifier of the study material. |
| `study_material.meaning_note` | body | `string` | no | Meaning notes specific for the subject. |
