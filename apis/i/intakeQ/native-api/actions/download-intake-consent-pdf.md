# Download Intake Consent PDF with IntakeQ

Retrieves an intake consent PDF from IntakeQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/intakes/{intakeId}/consent/{consentFormId}/pdf`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Download Intake Consent PDF](https://support.intakeq.com/article/31-intakeq-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intakeId` | path | `string` | yes | The IntakeQ intake form ID. |
| `consentFormId` | path | `string` | yes | The consent form ID associated with the intake. |
