# List Employee Training Records with BambooHR

Lists employee training records from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/training/record/employee/:employeeId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Employee Training Records](https://documentation.bamboohr.com/reference/list-employee-trainings)

## Requirements

- **OAuth scopes:** `training`
- **scope:** `training` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `number` | yes | The internal employee ID of the employee to get a list of trainings for. |
| `type` | query | `number` | no | Optional training type ID to filter records. Omitting this parameter returns all training records for the employee. |
