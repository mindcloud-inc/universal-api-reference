# Get Changed Employee Table Data with BambooHR

Retrieves changed employee table data from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/changed/tables/:table`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Changed Employee Table Data](https://documentation.bamboohr.com/reference/get-changed-employee-table-data)

## Requirements

- **OAuth scopes:** `employee employee:assets employee:compensation employee:custom_fields employee:custom_fields_encrypted employee:education employee:emergency_contacts employee:job sensitive_employee:creditcards`
- **scope:** `employee, employee:assets, employee:compensation, employee:custom_fields, employee:custom_fields_encrypted, employee:education, employee:emergency_contacts, employee:job, sensitive_employee:creditcards` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table` | path | `string` | yes | The API name of the table to retrieve changed data for. See the TableName schema for valid standard values; custom tables use a `custom` prefix. Use GET /api/v1/meta/tables to discover the complete list. |
| `since` | query | `date` | yes | ISO 8601 timestamp (URL-encoded). Only employees changed since this timestamp will be returned. |
