# Get Job Application Details with BambooHR

Retrieves job application details from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/applicant_tracking/applications/:applicationId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Job Application Details](https://documentation.bamboohr.com/reference/get-application-details)

## Requirements

- **OAuth scopes:** `hiring:applications`
- **scope:** `hiring:applications` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicationId` | path | `string` | yes | The ID of the application to retrieve details for. |
