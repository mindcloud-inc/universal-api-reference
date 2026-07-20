# Get Enriched Prospect Data with Hyperise

Retrieves enriched prospect data from Hyperise by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/data-enrichment`
- **Base URL:** `https://app.hyperise.io/api/v1/regular`
- **Official documentation:** [Get Enriched Prospect Data](https://hyperise.customerly.help/en/articles/9941-Data-Enrichment-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The email address to enrich. |
| `image_hash` | query | `string` | yes | The Hyperise image template hash used for enrichment fallback. |
