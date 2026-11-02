# Get Total Rewards Statement with BambooHR

Retrieves total rewards statement from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/total_rewards/:employeeId/statement`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Total Rewards Statement](https://documentation.bamboohr.com/reference/get-total-rewards-statement)

## Requirements

- **OAuth scopes:** `total_rewards`
- **scope:** `total_rewards` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID of the employee whose total rewards statement is returned. |
