# Run Search Volume and CPC Finder with Botster

Creates a Botster keyword search volume and CPC job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/google-keyword-search-volume`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Search Volume and CPC Finder](https://botster.io/bots/google-keyword-search-volume)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Search keywords and phrases. |
| `region_key` | body | `string` | yes | Region. |
