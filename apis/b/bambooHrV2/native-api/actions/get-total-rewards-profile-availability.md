# Get Total Rewards Profile Availability with BambooHR

Retrieves total rewards profile availability from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/compensation/total_rewards/:employeeId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Total Rewards Profile Availability](https://documentation.bamboohr.com/reference/check-total-rewards-profile)

## Requirements

- **OAuth scopes:** `total_rewards`
- **scope:** `total_rewards` — Required OAuth scope documented by BambooHR.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID of the employee to check. |
