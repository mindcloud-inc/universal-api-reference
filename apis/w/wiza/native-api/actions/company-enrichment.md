# Company Enrichment with Wiza

Retrieves enriched company data from Wiza.

## Endpoint

- **Method:** `POST`
- **Path:** `/company_enrichments`
- **Base URL:** `https://wiza.co/api`
- **Official documentation:** [Company Enrichment](https://docs.wiza.co/api-reference/company-enrichment/company-enrichment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | body | `string` | no | Company name to enrich. |
| `company_domain` | body | `string` | no | Company domain to enrich. |
| `company_linkedin_id` | body | `string` | no | LinkedIn company ID to enrich. |
| `company_linkedin_slug` | body | `string` | no | LinkedIn company slug to enrich. |
