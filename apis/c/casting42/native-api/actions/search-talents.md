# Search Talents with Casting42

Finds Casting42 talents by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/talents/find`
- **Base URL:** `https://casting42.com`
- **Official documentation:** [Search Talents](https://documenter.getpostman.com/view/24607394/2s9YR6buRP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Maximum number of talents to return. |
| `offset` | body | `number` | no | Number of records to skip before returning results. |
| `sort_field` | body | `string` | no | Field to sort by, such as updatedAt. |
| `sort_order` | body | `string` | no | Sort direction. Use asc or desc. |
| `query[]` | body | `array<object>` | yes | Array of search clauses. Each entry is one OR block of field filters. |
