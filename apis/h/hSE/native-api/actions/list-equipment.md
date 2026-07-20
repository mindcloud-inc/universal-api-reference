# List Equipment with 4HSE

Retrieves equipment from 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/equipment/index`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [List Equipment](https://docs.4hse.com/en/api/equipment/#operation-indexEquipment-post)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | Search filters. |
| `filter.office_id` | body | `string` | no | Filter by office ID. |
| `filter.project_id` | body | `string` | no | Filter by project ID. |
| `filter.name` | body | `string` | no | Filter by name. Maximum length: 255. |
| `history` | body | `boolean` | no | Include historicized equipment. |
