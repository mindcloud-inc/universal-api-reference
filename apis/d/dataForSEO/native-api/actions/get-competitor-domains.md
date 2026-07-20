# Get Competitor Domains with DataForSEO

Retrieves competitor domain data from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/dataforseo_labs/google/competitors_domain/live.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Competitor Domains](https://docs.dataforseo.com/v3/dataforseo_labs-google-competitors_domain-live/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | body | `string` | yes | Domain to analyze for competing domains. |
| `location_name` | body | `string` | no | Location context for the DataForSEO Labs analysis. |
| `language_code` | body | `string` | no | Language code for the analysis context. |
| `ignore_synonyms` | body | `boolean` | no | Exclude synonymous keywords from the comparison. |
