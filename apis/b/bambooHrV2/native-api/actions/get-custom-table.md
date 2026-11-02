# Get Custom Table with BambooHR

Retrieves custom table from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/hris/custom-tables/:customTableId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Custom Table](https://documentation.bamboohr.com/reference/get-custom-table)

## Requirements

- **OAuth scopes:** `employee:custom_fields`
- **scope:** `employee:custom_fields` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customTableId` | path | `string` | yes | The ID of the custom table to retrieve |
