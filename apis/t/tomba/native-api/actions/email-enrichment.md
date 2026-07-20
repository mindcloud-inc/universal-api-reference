# Email Enrichment with Tomba

Retrieves contact enrichment data from Tomba.

## Endpoint

- **Method:** `GET`
- **Path:** `/enrich`
- **Base URL:** `https://api.tomba.io/v1`
- **Official documentation:** [Email Enrichment](https://docs.tomba.io/api/finder#email-enrichment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | query | `string` | yes |
| `enrich_mobile` | query | `boolean` | no |
