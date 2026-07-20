# List Employee Assets with TalentHR

Retrieves an employee's assets from TalentHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/employees/:employee/assets`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [List Employee Assets](https://apidocs.talenthr.io/#02e7bc80-2b16-4278-be9e-325031754db8)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee` | path | `number` | yes | TalentHR employee ID. |
| `limit` | query | `number` | no | Maximum number of assets to return. |
| `offset` | query | `number` | no | Number of assets to skip. |
| `order` | query | `string` | no | Sort direction. |
| `sort` | query | `string` | no | Field to sort by. |
