# Search Google with SearchAPI - Google Search

Finds Google web search results in SearchAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://www.searchapi.io/api/v1`
- **Official documentation:** [Search Google](https://www.searchapi.io/docs/google)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search terms to send to Google. Supports Google operators like site:, inurl:, intitle:, AND, and OR. |
| `location` | query | `string` | no | Canonical Google location such as New York,United States. Use Find Supported Locations to discover valid values. |
| `device` | query | `string` | no | Google device profile for the search. |
| `gl` | query | `string` | no | Google country code for localization. Defaults to us when omitted by SearchAPI. |
| `hl` | query | `string` | no | Google interface language code. Defaults to en when omitted by SearchAPI. |
| `page` | query | `number` | no | Search results page to return. SearchAPI defaults to page 1. |
| `safe` | query | `string` | no | SafeSearch behavior. SearchAPI defaults to blur. |
| `time_period` | query | `string` | no | Restrict results to a supported relative time period such as last_day, last_week, or last_month. |
| `verbatim` | query | `boolean` | no | Force Google to use exact keywords and bypass automatic query modifications. |
| `kgmid` | query | `string` | no | Knowledge Graph entity identifier such as /m/02_286 or /g/11f555cn8l. |
| `uule` | query | `string` | no | Exact Google-encoded location. Do not use together with Location. |
| `lr` | query | `string` | no | Restrict results to document languages using Google lang_ values such as lang_en or lang_it\|lang_de. |
| `cr` | query | `string` | no | Restrict results to documents originating in a specific country using Google country restriction values. |
| `nfpr` | query | `string` | no | Set to 1 to exclude auto-corrected results. |
| `filter` | query | `string` | no | Set to 1 to enable duplicate-content and host-crowding filters, or 0 to disable them. |
| `time_period_min` | query | `string` | no | Start date for custom time filtering in MM/DD/YYYY format. |
| `time_period_max` | query | `string` | no | End date for custom time filtering in MM/DD/YYYY format. |
| `optimization_strategy` | query | `string` | no | Controls request optimization: performance by default, or ads for higher ad collection success rate. |
