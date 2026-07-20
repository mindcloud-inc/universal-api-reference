# Bulk Collect Clean Companies By IDs with Coresignal

Creates a bulk clean company collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/company_clean/ids`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Clean Companies By IDs](https://docs.coresignal.com/company-api/clean-company-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes |
