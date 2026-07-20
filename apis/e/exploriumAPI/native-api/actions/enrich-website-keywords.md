# Enrich Website Keywords with Explorium

Enriches businesses with website keywords in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/businesses/company_website_keywords/enrich`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Enrich Website Keywords](https://developers.explorium.ai/reference/businesses/enrichments/keyword_search_on_websites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | body | `string` | yes | The Explorium business identifier to enrich. |
| `parameters` | body | `object` | yes | Keyword enrichment parameters, including the required keywords array. |
