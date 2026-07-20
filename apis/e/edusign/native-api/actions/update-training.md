# Update Training with Edusign

Updates an existing training in Edusign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/trainings/:trainingId`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Update Training](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trainingId` | path | `string` | yes | Training ID |
| `NAME` | body | `string` | no | Training name |
| `START` | body | `string` | no | Start date of the training (format YYYY-MM-DD, ISO 8601) |
| `END` | body | `string` | no | End date of the training (format YYYY-MM-DD, ISO 8601) |
| `GOALS` | body | `string` | no | Training goals |
| `TAGS[]` | body | `array<string>` | no | — |
| `API_ID` | body | `string` | no | The ID of your API resource representing the training |
| `API_TYPE` | body | `string` | no | The name of your API from where you created the training |
| `REGISTRATION_OPTIONS` | body | `object` | no | — |
| `REGISTRATION_OPTIONS.pastSheets` | body | `boolean` | no | If you want to add the students to past attendance sheets |
| `REGISTRATION_OPTIONS.pastDocuments` | body | `boolean` | no | If you want to add the students to past documents |
| `REGISTRATION_OPTIONS.pastSurveys` | body | `boolean` | no | If you want to add the students to past surveys |
| `REGISTRATION_OPTIONS.futureSheets` | body | `boolean` | no | If you want to add the students to future attendance sheets |
| `REGISTRATION_OPTIONS.futureDocuments` | body | `boolean` | no | If you want to add the students to future documents |
| `REGISTRATION_OPTIONS.futureSurveys` | body | `boolean` | no | If you want to add the students to future surveys |
