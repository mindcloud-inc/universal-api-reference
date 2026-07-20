# Convert Company Names with Anyleads

Retrieves domain data for a company name from Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/convert-company-names`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Convert Company Names](https://docs.anyleads.com/product/en/enrichment-data-software-to-find-emails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | body | `string` | yes | Company name to convert into a domain or normalized company data. |
