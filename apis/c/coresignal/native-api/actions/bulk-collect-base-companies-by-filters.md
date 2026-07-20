# Bulk Collect Base Companies By Filters with Coresignal

Creates a bulk base company collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/company_base/filter`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Base Companies By Filters](https://docs.coresignal.com/company-api/base-company-api/endpoints/bulk-collect-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | Base Company bulk-collect filters object. |
| `limit` | body | `number` | no | Maximum number of companies to queue in the bulk data request. |
