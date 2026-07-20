# Get Opportunities with Datalyse

Retrieves a list of opportunities from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/opportunities/get.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Get Opportunities](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datefrom` | body | `string` | no | Start date for filtering results (optional, format: YYYY-MM-DD) |
| `dateto` | body | `string` | no | End date for filtering results (optional, format: YYYY-MM-DD) |
| `search_value` | body | `string` | no | Text to search for (optional) |
| `timezone` | body | `string` | no | Timezone for date filtering (optional, example: Europe/Madrid) |
| `var_agentfilter` | body | `string` | no | Show only results for this agent ID (optional) |
| `var_page` | body | `string` | no | Page number |
| `var_resultspage` | body | `string` | no | Maximum number of results to display |
| `var_status` | body | `string` | no | Show only results with this status (optional) |
