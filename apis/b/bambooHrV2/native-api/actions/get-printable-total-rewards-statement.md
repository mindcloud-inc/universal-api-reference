# Get Printable Total Rewards Statement with BambooHR

Retrieves printable total rewards statement from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/total_rewards/:employeeId/printable`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Printable Total Rewards Statement](https://documentation.bamboohr.com/reference/get-total-rewards-printable-statement)

## Requirements

- **OAuth scopes:** `total_rewards`
- **scope:** `total_rewards` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID of the employee whose printable Total Rewards statement is returned. |
| `multiplier` | query | `number` | no | Hours-per-week multiplier for annualizing hourly pay. |
| `year` | query | `number` | no | Statement year. Defaults to the current year when omitted. |
