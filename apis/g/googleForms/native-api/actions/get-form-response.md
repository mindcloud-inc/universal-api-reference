# Get Form Response with Google Forms

Retrieves a form response from Google Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/:formId/responses/:responseId`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Get Form Response](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms.responses/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `responseId` | path | `string` | yes | The response identifier. |
