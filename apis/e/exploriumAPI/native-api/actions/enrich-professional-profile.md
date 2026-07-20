# Enrich Professional Profile with Explorium

Enriches prospects with professional profile data in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/prospects/profiles/enrich`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Enrich Professional Profile](https://developers.explorium.ai/reference/prospects/enrichments/professional_profile_contact_and_workplace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prospect_id` | body | `string` | yes | The Explorium prospect identifier to enrich. |
