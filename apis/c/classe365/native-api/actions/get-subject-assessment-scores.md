# Get Subject Assessment Scores with Classe365

Retrieves assessment scores for one subject from Classe365.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/subjectScore`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Get Subject Assessment Scores](https://speca.io/classe365/academics#get-assessments-score-for-subject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acds_id` | query | `string` | no | Academic session id. |
| `id` | query | `string` | no | Subject id. |
