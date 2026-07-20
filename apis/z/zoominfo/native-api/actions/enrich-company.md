# Enrich Company with Zoominfo

Enriches a company with ZoomInfo data.

## Endpoint

- **Method:** `POST`
- **Path:** `enrich/company`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [Enrich Company](https://api-docs.zoominfo.com/#59a59d9e-7eb9-44fa-904a-f10f9ab7c5fd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `matchCompanyInput[]` | body | `array<object>` | yes | Array of company match objects. Each object can include fields such as companyId, companyName, companyWebsite, companyTicker, companyPhone, or companyCountry. |
| `outputFields[]` | body | `array<string>` | no | Array of response field names to return. Send multiple values as a array. |
