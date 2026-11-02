# List Employee Time Off Policies V1 1 with BambooHR

Lists employee time off policies v1 1 from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1_1/employees/:employeeId/time_off/policies`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Employee Time Off Policies V1 1](https://documentation.bamboohr.com/reference/list-employee-time-off-policies-v1_1)

## Requirements

- **OAuth scopes:** `time_off`
- **scope:** `time_off` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID. |
