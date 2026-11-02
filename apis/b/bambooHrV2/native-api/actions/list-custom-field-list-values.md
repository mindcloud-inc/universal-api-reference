# List Custom Field List Values with BambooHR

Lists custom field list values from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/hris/custom-fields/:customFieldId/list-values`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Custom Field List Values](https://documentation.bamboohr.com/reference/list-custom-field-list-values)

## Requirements

- **OAuth scopes:** `employee:custom_fields`
- **scope:** `employee:custom_fields` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customFieldId` | path | `string` | yes | The ID of the custom field. |
