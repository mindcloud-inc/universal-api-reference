# Resend Questionnaire with IntakeQ

Resends a questionnaire from IntakeQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/intakes/resend`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Resend Questionnaire](https://support.intakeq.com/article/31-intakeq-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `IntakeId` | body | `string` | yes | The IntakeQ intake form ID. |
