# Get Employee Onboarding Experience by ID with BambooHR

Retrieves employee onboarding experience by id from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/:employeeId/onboarding-experiences/:onboardingExperienceId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Employee Onboarding Experience by ID](https://documentation.bamboohr.com/reference/180314d815c8b991c1e07c8e32851639)

## Requirements

- **OAuth scopes:** `onboarding`
- **scope:** `onboarding` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `employeeId` | path | `number` | yes |
| `onboardingExperienceId` | path | `number` | yes |
