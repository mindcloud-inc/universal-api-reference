# Bulk Collect Clean Companies By URLs with Coresignal

Creates a bulk clean company URL collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/company_clean/urls`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Clean Companies By URLs](https://docs.coresignal.com/company-api/clean-company-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes |
