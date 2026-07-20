# Create Text Question with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/question/save`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Create Text Question](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey that will contain the question. |
| `sectionId` | body | `string` | yes | Section that will contain the question. |
| `question` | body | `string` | yes | Text prompt for the question. |
