# Send Questionnaire with IntakeQ

Creates a questionnaire request in IntakeQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/intakes/send`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Send Questionnaire](https://support.intakeq.com/article/31-intakeq-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `QuestionnaireId` | body | `string` | yes | The IntakeQ questionnaire template ID. |
| `ClientId` | body | `string` | yes | The IntakeQ numeric client ID. |
