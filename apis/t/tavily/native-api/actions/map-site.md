# Map Site with Tavily

Maps a website from a base URL with Tavily.

## Endpoint

- **Method:** `POST`
- **Path:** `/map`
- **Base URL:** `https://api.tavily.com`
- **Official documentation:** [Map Site](https://docs.tavily.com/documentation/api-reference/endpoint/map)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allow_external` | body | `boolean` | no | Whether to include external domain links in the discovered URLs. |
| `exclude_domains[]` | body | `array<string>` | no | Regex patterns to exclude specific domains or subdomains. |
| `exclude_paths[]` | body | `array<string>` | no | Regex patterns to exclude specific URL paths. |
| `include_usage` | body | `boolean` | no | Include credit usage information in the response. |
| `limit` | body | `number` | no | Total number of links the mapper will process before stopping. |
| `max_breadth` | body | `number` | no | Max number of links to follow per page. |
| `max_depth` | body | `number` | no | Max depth of the mapping from the root URL. |
| `select_domains[]` | body | `array<string>` | no | Regex patterns to include only specific domains or subdomains. |
| `select_paths[]` | body | `array<string>` | no | Regex patterns to include only specific URL paths. |
| `timeout` | body | `number` | no | Maximum time in seconds to wait for the map operation before timing out. |
| `url` | body | `string` | yes | The root URL to begin the site map discovery. |
