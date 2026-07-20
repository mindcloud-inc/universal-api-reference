# LinkedIn Finder with Tomba

Finds contact details from LinkedIn in Tomba.

## Endpoint

- **Method:** `GET`
- **Path:** `/linkedin`
- **Base URL:** `https://api.tomba.io/v1`
- **Official documentation:** [LinkedIn Finder](https://docs.tomba.io/api/finder#linkedin-finder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `url` | query | `string` | yes |
| `enrich_mobile` | query | `boolean` | no |
| `full` | query | `boolean` | no |
