# List Company Job Openings with PredictLeads

Retrieves job openings for a PredictLeads company.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:company_id_or_domain/job_openings`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Company Job Openings](https://docs.predictleads.com/api_endpoints/job_openings_dataset/retrieve_company_s_job_openings)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id_or_domain` | path | `string` | yes | Company's ID or domain. |
| `active_only` | query | `boolean` | no | Return only active job openings. |
| `categories` | query | `string` | no | Comma-separated job opening categories. |
| `first_seen_at_from` | query | `string` | no | Include job openings first seen on or after this date. |
| `first_seen_at_until` | query | `string` | no | Include job openings first seen on or before this date. |
| `last_seen_at_from` | query | `string` | no | Include job openings last seen on or after this date. |
| `last_seen_at_until` | query | `string` | no | Include job openings last seen on or before this date. |
| `not_closed` | query | `boolean` | no | Exclude closed job openings. |
| `with_description_only` | query | `boolean` | no | Return only job openings that include a description. |
| `with_location_only` | query | `boolean` | no | Return only job openings that include a location. |
