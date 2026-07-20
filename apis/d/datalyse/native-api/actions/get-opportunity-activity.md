# Get Opportunity Activity with Datalyse

Retrieves activity for an opportunity from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/opportunities/getactivity.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Get Opportunity Activity](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunity_id` | body | `string` | yes | ID of the opportunity |
| `type` | body | `string` | no | Filter by activity type (optional) |
| `var_page` | body | `string` | no | Page number |
| `var_resultspage` | body | `string` | no | Maximum number of results to display |
