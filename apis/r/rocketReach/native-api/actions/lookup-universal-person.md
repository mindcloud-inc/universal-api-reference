# Lookup Universal Person with RocketReach

Retrieves a person from RocketReach Universal lookup.

## Endpoint

- **Method:** `GET`
- **Path:** `/universal/person/lookup`
- **Base URL:** `https://api.rocketreach.co/api/v2`
- **Official documentation:** [Lookup Universal Person](https://docs.rocketreach.co/reference/create_universal_person_lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `current_employer` | query | `string` | no | Current employer of the desired profile. Must be specified along with Name. |
| `email` | query | `string` | no | An email address for the desired profile. |
| `id` | query | `number` | no | RocketReach internal unique profile ID. |
| `linkedin_ext_url` | query | `string` | no | Deprecated: use LinkedIn URL. |
| `linkedin_url` | query | `string` | no | LinkedIn URL of the desired profile. |
| `name` | query | `string` | no | Name of the desired profile. Must be specified along with Current Employer. |
| `npi_number` | query | `number` | no | An NPI number for the desired profile, for US healthcare professionals. |
| `title` | query | `string` | no | Job title of the desired profile. |
| `webhook_id` | query | `number` | no | Webhook ID to receive lookup results. |
| `return_cached_emails` | query | `boolean` | no | Whether cached emails can be included while the lookup is still in progress. |
| `reveal_detailed_person_enrichment` | query | `boolean` | no | Whether to reveal detailed person enrichment data. |
| `reveal_healthcare_enrichment` | query | `boolean` | no | Whether to reveal healthcare enrichment data. |
| `reveal_personal_email` | query | `boolean` | no | Whether to reveal personal email enrichment data. |
| `reveal_phone` | query | `boolean` | no | Whether to reveal phone enrichment data. |
| `reveal_professional_email` | query | `boolean` | no | Whether to reveal professional email enrichment data. |
