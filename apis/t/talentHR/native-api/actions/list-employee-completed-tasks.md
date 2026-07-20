# List Employee Completed Tasks with TalentHR

Retrieves an employee's completed tasks from TalentHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/employees/:employee/tasks/completed`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [List Employee Completed Tasks](https://apidocs.talenthr.io/#d548c77b-91eb-43ba-98bf-a04dfbb43e5d)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee` | path | `number` | yes | TalentHR employee ID. |
| `limit` | query | `number` | no | Maximum number of tasks to return. |
| `offset` | query | `number` | no | Number of tasks to skip. |
| `order` | query | `string` | no | Sort direction. |
| `sort` | query | `string` | no | Field to sort by. |
