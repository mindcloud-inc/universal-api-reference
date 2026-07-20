# Get Changed Employees with BambooHR

Retrieves changed employee IDs from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/changed/[:type]`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Get Changed Employees](https://documentation.bamboohr.com/reference/changed-employee-ids)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `string` | yes | Return employees changed after this ISO-8601 timestamp. |
| `type` | path | `string` | no | Optional change type filter. Use inserted, updated, or deleted. |
