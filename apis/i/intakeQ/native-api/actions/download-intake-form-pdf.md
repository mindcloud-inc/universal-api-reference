# Download Intake Form PDF with IntakeQ

Retrieves an intake form PDF from IntakeQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/intakes/{intakeId}/pdf`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Download Intake Form PDF](https://support.intakeq.com/article/31-intakeq-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intakeId` | path | `string` | yes | The IntakeQ intake form ID. |
