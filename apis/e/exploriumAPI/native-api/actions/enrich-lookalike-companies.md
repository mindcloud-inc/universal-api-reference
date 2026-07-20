# Enrich Lookalike Companies with Explorium

Enriches businesses with lookalike companies in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/businesses/lookalikes/enrich`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Enrich Lookalike Companies](https://developers.explorium.ai/reference/businesses/enrichments/lookalike-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | body | `string` | yes | The Explorium business identifier to enrich. |
