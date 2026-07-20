# Create Section Header Item with Google Forms

Creates a section header item in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Section Header Item](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | yes | Title shown at the top of the new section/page break. |
| `description` | body | `string` | no | Optional section description. |
| `locationIndex` | body | `number` | yes | Where to place the new section in the form. |
