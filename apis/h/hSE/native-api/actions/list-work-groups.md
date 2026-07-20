# List Work Groups with 4HSE

Retrieves work groups from 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/work-group/index`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [List Work Groups](https://docs.4hse.com/en/api/workgroup/#operation-indexWorkGroup-post)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | Search filters. |
| `filter.office_id` | body | `string` | no | Filter by office ID. |
| `filter.work_group_type` | body | `string` | no | Filter by work group type. |
| `filter.name` | body | `string` | no | Filter by name. Maximum length: 255. |
| `filter.project_id` | body | `string` | no | Filter by project ID. |
| `history` | body | `boolean` | no | Include historicized work groups. |
