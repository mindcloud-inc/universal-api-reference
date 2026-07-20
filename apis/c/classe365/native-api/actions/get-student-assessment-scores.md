# Get Student Assessment Scores with Classe365

Retrieves assessment scores for one student from Classe365.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/studentScore`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Get Student Assessment Scores](https://speca.io/classe365/academics#get-assessment-score-for-student)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acds_id` | query | `string` | no | Academic session id. |
| `id` | query | `string` | no | Student id. |
