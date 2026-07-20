# Create Study Material with WaniKani

Creates a new study material in WaniKani.

## Endpoint

- **Method:** `POST`
- **Path:** `/study_materials`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [Create Study Material](https://docs.api.wanikani.com/20170710/#create-a-study-material)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_material.subject_id` | body | `number` | yes | Unique identifier of the subject. |
| `study_material.meaning_note` | body | `string` | no | Meaning notes specific for the subject. |
