# List Employee Managers with TalentHR

Retrieves an employee's managers from TalentHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/employees/:employee/managers`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [List Employee Managers](https://apidocs.talenthr.io/#e8816c2b-22f2-4a0e-b329-aa841d42261c)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee` | path | `number` | yes | TalentHR employee ID. |
