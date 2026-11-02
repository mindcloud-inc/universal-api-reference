# List Employee Files with BambooHR

Lists employee files from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/:id/files/view`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Employee Files](https://documentation.bamboohr.com/reference/list-employee-files)

## Requirements

- **OAuth scopes:** `employee:file`
- **scope:** `employee:file` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The internal employee ID of the employee whose files are being listed. |
