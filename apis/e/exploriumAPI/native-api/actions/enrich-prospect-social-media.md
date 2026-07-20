# Enrich Prospect Social Media with Explorium

Enriches prospects with social media in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/prospects/linkedin_posts/enrich`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Enrich Prospect Social Media](https://developers.explorium.ai/reference/prospects/enrichments/individual_social_media_presence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prospect_id` | body | `string` | yes | The Explorium prospect identifier to enrich. |
