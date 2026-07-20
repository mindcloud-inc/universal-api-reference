# Enrich People with Captain Data

Retrieves detailed person data from Captain Data by LinkedIn URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/enrich`
- **Base URL:** `https://api.captaindata.com/v1`
- **Official documentation:** [Enrich People](https://docs.captaindata.com/v1/api/people/enrich)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `li_profile_url` | query | `string` | yes | LinkedIn profile URL to enrich. |
| `full_enrich` | query | `boolean` | no | Include additional experiences, skills, and education details. |
