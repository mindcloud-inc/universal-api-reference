# List Contacts with GetSales.io

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/api/leads/search`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [List Contacts](https://api.getsales.io/api/openapi/contacts/searchcontacts.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | Filters to apply when searching contacts. |
| `limit` | body | `number` | no | Number of contacts to return. |
| `offset` | body | `number` | no | Number of contacts to skip. |
| `order_field` | body | `string` | no | Field to sort by. |
| `order_type` | body | `list` | no | Sorting direction. Accepted values: `0`, `1`. |
| `disable_aggregation` | body | `boolean` | no | When true, disables contact data aggregation. |
