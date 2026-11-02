# List Employee Table Rows with BambooHR

Lists employee table rows from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/:id/tables/:table`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Employee Table Rows](https://documentation.bamboohr.com/reference/get-employee-table-data)

## Requirements

- **OAuth scopes:** `employee employee:assets employee:compensation employee:custom_fields employee:custom_fields_encrypted employee:education employee:emergency_contacts employee:job employee:job.write sensitive_employee:creditcards`
- **scope:** `employee, employee:assets, employee:compensation, employee:custom_fields, employee:custom_fields_encrypted, employee:education, employee:emergency_contacts, employee:job, employee:job.write, sensitive_employee:creditcards` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The internal employee ID. Use the special value "all" to retrieve table data for all employees the authenticated caller has access to. |
| `table` | path | `string` | yes | The API name of the table to retrieve. See the TableName schema for standard values; custom tables also accepted (e.g., `custom1`, `custom42`). Use the `list-tabular-fields` tool (GET /api/v1/meta/tables) to discover custom table names. |
