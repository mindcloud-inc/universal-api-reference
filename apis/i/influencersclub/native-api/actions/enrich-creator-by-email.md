# Enrich Creator By Email with Influencers.club

Retrieves creator enrichment data from Influencers.club by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/creators/enrich/email/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Enrich Creator By Email](https://docs.influencers.club/openapi/enrich-by-email/public_v1_creators_enrich_email_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Creator email address. |
