# Get Employee File with BambooHR

Retrieves employee file from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/:id/files/:fileId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Employee File](https://documentation.bamboohr.com/reference/get-employee-file)

## Requirements

- **OAuth scopes:** `employee:file`
- **scope:** `employee:file` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The internal employee ID of the employee whose file is being retrieved. Use 0 to resolve to the employee associated with the authenticated caller. |
| `fileId` | path | `number` | yes | The ID of the employee file to download. |
