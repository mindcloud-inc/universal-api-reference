# Enrich Company with DataForB2B

Retrieves enriched company data from DataForB2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/enrich/company`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Enrich Company](https://docs.dataforb2b.ai/api-reference/enrich-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_identifier` | body | `string` | yes | Company name, domain, LinkedIn URL, or company ID to enrich. |
