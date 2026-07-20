# Update Practitioner with IntakeQ

Updates an existing practitioner in IntakeQ.

## Endpoint

- **Method:** `PUT`
- **Path:** `/practitioners`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Update Practitioner](https://support.intakeq.com/article/433-intakeq-partner-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `string` | yes | The practitioner ID. |
| `FirstName` | body | `string` | yes | The practitioner's first name. |
| `LastName` | body | `string` | yes | The practitioner's last name. |
| `Email` | body | `string` | yes | The practitioner's email address. |
| `RoleName` | body | `string` | yes | The IntakeQ role name. |
