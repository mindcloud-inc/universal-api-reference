# Create Question with CodeREADr

Creates a new data collection question in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Create Question](https://secure.codereadr.com/apidocs/Questions.md#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `question_text` | body | `string` | yes | Text for the new question. |
| `question_type` | body | `string` | no | Optional type such as manual, option, dropdown, or gps. |
