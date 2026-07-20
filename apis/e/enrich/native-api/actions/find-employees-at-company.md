# Find Employees At A Company with Enrich.so

Finds company employees in Enrich.so by LinkedIn URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/people-search/employee-finder`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Find Employees At A Company](https://doc.enrich.so/find-employees-at-a-company-28537860e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_linkedin_url` | body | `string` | yes | LinkedIn company URL to search. |
| `country[]` | body | `array<string>` | no | Optional country filters. |
| `max_results` | body | `number` | no | Results per page, 1-100. |
| `page` | body | `number` | no | Page number, starting at 1. |
