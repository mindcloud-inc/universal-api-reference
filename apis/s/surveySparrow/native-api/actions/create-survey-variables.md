# Create Survey Variables with SurveySparrow

Creates survey variables in SurveySparrow.

## Endpoint

- **Method:** `POST`
- **Path:** `/variables/batch`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Create Survey Variables](https://developers.surveysparrow.com/rest-apis/post-v-3-variables-batch/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | body | `number` | yes | ID of survey |
| `variables[]` | body | `array<object>` | yes | Array of variable objects |
