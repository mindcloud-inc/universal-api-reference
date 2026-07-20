# Upsert Assessment Score with Classe365

Creates or updates an assessment score in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/saveAssessmentScore`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Upsert Assessment Score](https://speca.io/classe365/academics#add-update-assessment-score)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acds_id` | body | `string` | no | Academic session id. |
| `assessment_id` | body | `string` | no | Assessment id. |
| `score_data` | body | `string` | no | JSON map of student scores. |
| `subject_id` | body | `string` | no | Subject id. |
