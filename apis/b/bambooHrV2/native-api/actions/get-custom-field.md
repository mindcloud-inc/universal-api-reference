# Get Custom Field with BambooHR

Retrieves custom field from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/hris/custom-fields/:customFieldId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Custom Field](https://documentation.bamboohr.com/reference/get-custom-field)

## Requirements

- **OAuth scopes:** `employee:custom_fields`
- **scope:** `employee:custom_fields` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customFieldId` | path | `string` | yes | The ID of the custom field to retrieve |
