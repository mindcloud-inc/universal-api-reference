# Update Survey Settings with Porsline

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/surveys/:survey_id/settings/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Update Survey Settings](https://developers.porsline.com/#tag/Settings/paths/~1api~1surveys~1{survey_id}~1settings~1/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `hide_progressbar` | body | `boolean` | no | Whether to hide the survey progress bar. |
