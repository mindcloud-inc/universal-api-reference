# List Survey Responses with Survser

## Endpoint

- **Method:** `GET`
- **Path:** `/response/list`
- **Base URL:** `https://survser.com/api/public/`
- **Official documentation:** [List Survey Responses](https://docs.survser.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | query | `string` | yes | The Survser survey ID. Survser docs say you can find it in the survey insights URL `survser.com/surveys/<id>/insights`. |
