# Create Survey From Template with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/survey/cloneSurveyTemplate`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Create Survey From Template](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `string` | yes | Template identifier to clone into a new survey. |
| `name` | body | `string` | no | Name for the created survey. |
| `category` | body | `string` | no | Optional category for the created survey. |
