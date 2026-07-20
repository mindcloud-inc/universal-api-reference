# Create Variable with SurveySparrow

Creates a survey variable in SurveySparrow.

## Endpoint

- **Method:** `POST`
- **Path:** `/variables`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Create Variable](https://developers.surveysparrow.com/rest-apis/post-v-3-variables/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | body | `number` | yes | ID of survey |
| `label` | body | `string` | yes | Variable label |
| `name` | body | `string` | yes | Unique variable name |
| `description` | body | `string` | no | Variable description |
| `type` | body | `list` | yes | Variable type |
