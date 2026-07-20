# Search Appointments with HIPAAtizer

Finds appointments in HIPAAtizer by location, service, or date.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/api_key/appointments/search`
- **Base URL:** `https://app.hipaatizer.com`
- **Official documentation:** [Search Appointments](https://github.com/HIPAAtizer/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | no | Optional raw request wrapper. Use `{}` when running without filters. |
| `request.dateRange.from` | body | `string` | no | Start date filter. |
| `request.dateRange.to` | body | `string` | no | End date filter. |
| `request.locationIds` | body | `list<string>` | no | Optional location UUID filters. |
| `request.pagination.limit` | body | `number` | no | Pagination page size. |
| `request.pagination.page` | body | `number` | no | Pagination page number. |
| `request.search` | body | `string` | no | Search term. |
| `request.serviceIds` | body | `list<string>` | no | Optional service UUID filters. |
| `request.workerIds` | body | `list<string>` | no | Optional worker UUID filters. |
