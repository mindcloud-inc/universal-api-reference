# Find Addresses with Address Auto-Complete by Fetchify

Finds address matches in Fetchify by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/find`
- **Base URL:** `https://api.craftyclicks.co.uk/address/1.1`
- **Official documentation:** [Find Addresses](https://docs.fetchify.com/json-api/address-auto-complete.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | The partial address or postcode to autocomplete. |
| `country` | query | `string` | yes | Three-letter Fetchify country code such as `gbr` or `usa`. |
| `id` | query | `string` | no | Optional grouping identifier returned by a previous find call. |
| `extra.best_match_only` | query | `boolean` | no | Return only the top autocomplete match. |
| `extra.no_groupings` | query | `boolean` | no | Disable grouped results in the autocomplete response. |
| `extra.exclude_pobox` | query | `boolean` | no | Exclude PO box style matches. |
| `extra.exclude_areas` | query | `list<string>` | no | Optional list of areas to exclude from autocomplete results. |
