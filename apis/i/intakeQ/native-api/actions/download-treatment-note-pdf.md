# Download Treatment Note PDF with IntakeQ

Retrieves a treatment note PDF from IntakeQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/notes/{noteId}/pdf`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Download Treatment Note PDF](https://support.intakeq.com/article/342-intakeq-notes-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `noteId` | path | `string` | yes | The IntakeQ treatment note ID. |
