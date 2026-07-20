# List Offices with 4HSE

Retrieves offices from 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/office/index`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [List Offices](https://docs.4hse.com/en/api/office/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | Office filters. |
| `filter.project_id` | body | `string` | no | Find offices within a company. |
| `filter.name` | body | `string` | no | Search an office by name within a project. |
| `filter.office_type_icon` | body | `string` | no | Filter by office type icon. |
| `history` | body | `boolean` | no | Include historized entries when true. |
