# Deduplicate Names with Rosette Text Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `/name-deduplication`
- **Base URL:** `https://api.rosette.com/rest/v1`
- **Official documentation:** [Deduplicate Names](https://docs.babelstreet.com/en/index-en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `names[]` | body | `array<object>` | yes | List of names to deduplicate. |
| `threshold` | body | `number` | no | Similarity threshold for duplicate grouping. |
