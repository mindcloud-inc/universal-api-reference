# Enrich Webstack with Explorium

Enriches businesses with webstack data in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/businesses/webstack/enrich`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Enrich Webstack](https://developers.explorium.ai/reference/businesses/enrichments/webstack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | body | `string` | yes | The Explorium business identifier to enrich. |
