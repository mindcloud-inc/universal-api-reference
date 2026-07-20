# Move Question To Section with Google Forms

Moves a question into a section in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Move Question To Section](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `originalIndex` | body | `number` | yes | Current index of the question item to move. |
| `sectionIndex` | body | `number` | yes | Destination section/page break index. |
