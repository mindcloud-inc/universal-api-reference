# List People with 4HSE

Retrieves people from 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/person/index`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [List People](https://docs.4hse.com/en/api/person/#operation-indexPerson-post)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | Search filters. |
| `filter.project_id` | body | `string` | no | Filter by project ID. |
| `filter.last_name` | body | `string` | no | Filter by last name. Maximum length: 70. |
| `filter.code` | body | `string` | no | Filter by employee code. Maximum length: 50. |
| `filter.tax_code` | body | `string` | no | Filter by tax code. Maximum length: 30. |
| `filter.is_employee` | body | `number` | no | Filter employees only. |
| `history` | body | `boolean` | no | Include historicized people. |
