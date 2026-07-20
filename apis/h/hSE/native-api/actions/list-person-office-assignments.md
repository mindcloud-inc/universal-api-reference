# List PersonOffice Assignments with 4HSE

Retrieves person-office assignments from 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/person-office/index`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [List PersonOffice Assignments](https://docs.4hse.com/en/api/personoffice/#operation-indexPersonOffice-post)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | Search filters. |
| `filter.office_id` | body | `string` | no | Filter by office ID. |
| `filter.person_id` | body | `string` | no | Filter by person ID. |
| `filter.project_id` | body | `string` | no | Filter by project ID. |
| `filter.person_last_name` | body | `string` | no | Filter by person last name. Maximum length: 70. |
| `filter.person_tax_code` | body | `string` | no | Filter by person tax code. Maximum length: 30. |
| `history` | body | `boolean` | no | Include historicized assignments. |
