# List Employee Pending Tasks with TalentHR

Retrieves an employee's pending tasks from TalentHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/employees/:employee/tasks/pending`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [List Employee Pending Tasks](https://apidocs.talenthr.io/#e90d17c5-0e6b-47ad-b69b-96048515126d)

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
