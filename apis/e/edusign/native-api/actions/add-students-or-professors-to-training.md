# Add Students Or Professors To Training with Edusign

Adds students or professors to a training in Edusign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/trainings/resources/:trainingId`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Add Students Or Professors To Training](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trainingId` | path | `string` | yes | The unique ID of the training |
| `studentsIds[]` | body | `array<string>` | no | — |
| `professorsIds[]` | body | `array<string>` | no | — |
| `options` | body | `object` | no | — |
| `options.pastSheets` | body | `boolean` | no | If you want to add the students to past attendance sheets |
| `options.pastDocuments` | body | `boolean` | no | If you want to add the students to past documents |
| `options.pastSurveys` | body | `boolean` | no | If you want to add the students to past surveys |
| `options.futureSheets` | body | `boolean` | no | If you want to add the students to future attendance sheets |
| `options.futureDocuments` | body | `boolean` | no | If you want to add the students to future documents |
| `options.futureSurveys` | body | `boolean` | no | If you want to add the students to future surveys |
