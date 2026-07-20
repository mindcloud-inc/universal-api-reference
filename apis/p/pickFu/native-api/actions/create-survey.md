# Create Survey with PickFu

## Endpoint

- **Method:** `POST`
- **Path:** `/surveys`
- **Base URL:** `https://api.pickfu.com/v1`
- **Official documentation:** [Create Survey](https://www.pickfu.com/docs/api-reference/surveys/create-survey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `questions[]` | body | `array<object>` | yes | List of questions for the survey. |
| `targeting[]` | body | `array<string>` | no | Demographic targeting traits. |
| `reporting[]` | body | `array<string>` | no | Reporting breakdown traits. |
| `country` | body | `string` | no | Two-letter country code. |
| `sample_size` | body | `string` | no | Number of respondents. |
| `survey_intent` | body | `string` | no | Original intent of the survey as interpreted by AI. |
| `is_mini_poll` | body | `boolean` | no | Whether to create this survey as a daily mini-poll. |
