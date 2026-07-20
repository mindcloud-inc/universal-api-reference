# Get Leads with Datalyse

Retrieves contacts or companies from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/leads/get.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Get Leads](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `control_filter_email` | body | `string` | no | Filter by contact email (optional) |
| `control_filter_name` | body | `string` | no | Filter by contact name (optional) |
| `datefrom` | body | `string` | no | Start date for filtering results (optional, format: YYYY-MM-DD) |
| `dateto` | body | `string` | no | End date for filtering results (optional, format: YYYY-MM-DD) |
| `filter_types` | body | `string` | no | Filter type for the search value (optional) |
| `search_value` | body | `string` | no | Text to search for (optional) |
| `timezone` | body | `string` | no | Timezone for date filtering (optional, example: Europe/Madrid) |
| `var_agentfilter` | body | `string` | no | Show only results for this agent ID (optional) |
| `var_page` | body | `string` | no | Page number |
| `var_resultspage` | body | `string` | no | Maximum number of results to display |
| `var_status` | body | `string` | no | Show only results with this status (optional) |
