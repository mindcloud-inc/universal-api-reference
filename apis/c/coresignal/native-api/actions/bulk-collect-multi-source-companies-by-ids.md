# Bulk Collect Multi-source Companies By IDs with Coresignal

Creates a bulk multi-source company collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/company_multi_source/ids`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Multi-source Companies By IDs](https://docs.coresignal.com/company-api/multi-source-company-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes |
