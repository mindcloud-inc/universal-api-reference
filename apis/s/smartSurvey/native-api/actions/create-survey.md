# Create Survey with SmartSurvey

Creates a new survey in SmartSurvey.

## Endpoint

- **Method:** `POST`
- **Path:** `/surveys`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Create Survey](https://docs.smartsurvey.io/reference/post_surveys)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | The title for the new survey |
| `language_id` | body | `number` | no | The language id for the new survey |
| `theme_id` | body | `number` | no | The theme id for the new survey |
| `folder_id` | body | `number` | no | The folder id for the new survey |
