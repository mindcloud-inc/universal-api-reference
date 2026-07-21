# Create Question Item with Google Forms

Creates a question item in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Question Item](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | yes | Question item title. |
| `question` | body | `object` | yes | Full Google Forms Question object for advanced question types. |
| `locationIndex` | body | `number` | yes | Where to place the new question item. |
| `description` | body | `string` | no | — |
