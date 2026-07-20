# Enrich Company Ratings with Explorium

Enriches businesses with company ratings in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/businesses/company_ratings_by_employees/enrich`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Enrich Company Ratings](https://developers.explorium.ai/reference/businesses/enrichments/company_ratings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | body | `string` | yes | The Explorium business identifier to enrich. |
