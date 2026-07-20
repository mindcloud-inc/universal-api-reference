# Create Survey With AI Builder with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/generateSurvey/generateSurvey`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Create Survey With AI Builder](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Survey brief or prompt for the AI builder. |
| `name` | body | `string` | no | Name for the AI-built survey. |
| `category` | body | `string` | no | Optional category for the AI-built survey. |
