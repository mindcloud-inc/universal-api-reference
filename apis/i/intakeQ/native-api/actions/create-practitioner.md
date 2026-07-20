# Create Practitioner with IntakeQ

Creates a new practitioner in IntakeQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/practitioners`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Create Practitioner](https://support.intakeq.com/article/433-intakeq-partner-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FirstName` | body | `string` | yes | The practitioner's first name. |
| `LastName` | body | `string` | yes | The practitioner's last name. |
| `Email` | body | `string` | yes | The practitioner's email address. |
| `RoleName` | body | `string` | yes | The IntakeQ role name. |
