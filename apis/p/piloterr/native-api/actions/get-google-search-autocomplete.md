# Get Google Search Autocomplete with Piloterr

## Endpoint

- **Method:** `GET`
- **Path:** `/google/search/autocomplete`
- **Base URL:** `https://api.piloterr.com/v2`
- **Official documentation:** [Get Google Search Autocomplete](https://docs.piloterr.com/google-search-autocomplete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gl` | query | `string` | no | Two-letter Google country code. |
| `hl` | query | `string` | no | Two-letter Google language code. |
| `query` | query | `string` | yes | Partial query for Google autocomplete. |
