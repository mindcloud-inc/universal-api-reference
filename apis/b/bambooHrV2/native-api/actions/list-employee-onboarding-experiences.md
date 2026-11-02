# List Employee Onboarding Experiences with BambooHR

Lists employee onboarding experiences from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/:employeeId/onboarding-experiences`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Employee Onboarding Experiences](https://documentation.bamboohr.com/reference/b678783b410374647b30c1e034d24f69)

## Requirements

- **OAuth scopes:** `onboarding`
- **scope:** `onboarding` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `employeeId` | path | `number` | yes |
