# Get Domain Rank Overview with DataForSEO

Retrieves domain rank overview data from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/dataforseo_labs/google/domain_rank_overview/live.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Domain Rank Overview](https://docs.dataforseo.com/v3/dataforseo_labs-google-domain_rank_overview-live/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | body | `string` | yes | Domain to analyze for rank overview. |
| `location_name` | body | `string` | no | Location context for the DataForSEO Labs analysis. |
| `language_code` | body | `string` | no | Language code for the analysis context. |
| `ignore_synonyms` | body | `boolean` | no | Exclude synonymous keywords from the overview. |
