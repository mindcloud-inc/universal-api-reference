# Update Task Date with AppWright

Updates a job task due date in AppWright.

## Endpoint

- **Method:** `POST`
- **Path:** `awAPI/awAPI.asp`
- **Base URL:** `https://{clientId}.AppWright.com`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `JobNumber` | query | `string` | no |
| `TaskDesc` | query | `string` | no |
| `DueDate` | query | `string` | no |
| `MoveOption` | query | `list` | no |
| `Status` | query | `list` | no |
