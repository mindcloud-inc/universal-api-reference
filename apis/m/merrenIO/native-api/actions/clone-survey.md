# Clone Survey with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/survey/cloneSurvey`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Clone Survey](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Existing survey to clone. |
| `name` | body | `string` | no | Optional name for the cloned survey. |
