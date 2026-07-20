# Enrich Company Master Data with Zoominfo

Enriches company master data with ZoomInfo data.

## Endpoint

- **Method:** `POST`
- **Path:** `enrich/company-master`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [Enrich Company Master Data](https://api-docs.zoominfo.com/#8b6cffe4-cb34-44ab-ad5d-1953d372ffd3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `matchCompanyInput[]` | body | `array<object>` | yes | Array of company master match objects using documented fields such as zi_c_url, zi_c_name, phone, address, email, or zi_c_company_id. |
| `outputFields[]` | body | `array<string>` | no | Array of response field names to return. Send multiple values as a array. |
