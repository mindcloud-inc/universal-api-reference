# Add Person with AssessTEAM

Creates a new person in AssessTEAM.

## Endpoint

- **Method:** `POST`
- **Path:** `/person/addperson`
- **Base URL:** `https://restapi.assessteam.com`
- **Official documentation:** [Add Person](https://restapi.assessteam.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstname` | query | `string` | yes | Person first name, for example Jon. |
| `lastname` | query | `string` | yes | Person last name, for example Doe. |
| `personcode` | query | `string` | yes | Unique person code, for example 1001. |
| `dateofjoining` | query | `string` | yes | Date of joining, for example 2026-04-07. |
| `email` | query | `string` | yes | Email address, for example sample1@yourcompany.com. |
| `contactnumber` | query | `string` | yes | Contact number, for example 1234567890. |
| `userpermissions` | query | `string` | no | User permission or role, for example Employee. |
| `team` | query | `string` | yes | Team assigned to person, for example Administration. |
| `jobtitle` | query | `string` | yes | Job title, for example QA Analyst. |
| `evaluators` | query | `string` | no | Person evaluator names, for example Jack Doe. |
| `flgIsSelfEvaluation` | query | `boolean` | yes | Enable self evaluation. |
