# Get Personal Data Counters with Survicate

Retrieves personal data counts by email from Survicate.

## Endpoint

- **Method:** `GET`
- **Path:** `/personal-data`
- **Base URL:** `https://data-api.survicate.com/v2`
- **Official documentation:** [Get Personal Data Counters](https://developers.survicate.com/data-export/personal-data/#get-personal-data-counters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The email address to search for across all data sources. |
