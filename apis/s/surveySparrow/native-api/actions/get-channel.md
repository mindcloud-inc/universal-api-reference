# Get Channel with SurveySparrow

Retrieves a channel from SurveySparrow.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/{{id}}`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Get Channel](https://developers.surveysparrow.com/rest-apis/get-v-3-channels-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Channel ID |
| `survey_id` | query | `number` | yes | Survey ID |
