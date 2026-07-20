# Get Company Activity with Datalyse

Retrieves activity for a company from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/companies/getactivity.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Get Company Activity](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_lead_id` | body | `string` | yes | ID of the company |
| `type` | body | `string` | no | Filter by activity type (optional) |
| `var_page` | body | `string` | no | Page number |
| `var_resultspage` | body | `string` | no | Maximum number of results to display |
