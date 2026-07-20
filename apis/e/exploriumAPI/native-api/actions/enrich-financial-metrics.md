# Enrich Financial Metrics with Explorium

Enriches businesses with financial metrics in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/businesses/financial_indicators/enrich`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Enrich Financial Metrics](https://developers.explorium.ai/reference/businesses/enrichments/financial_metrics_for_public_companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | body | `string` | yes | The Explorium business identifier to enrich. |
