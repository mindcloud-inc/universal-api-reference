# List Productions with Auphonic

Retrieves productions from Auphonic.

## Endpoint

- **Method:** `GET`
- **Path:** `/productions.json`
- **Base URL:** `https://auphonic.com/api`
- **Official documentation:** [List Productions](https://auphonic.com/help/api/query.html#list-all-productions-and-presets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `minimal_data` | query | `boolean` | no | Return a smaller production payload. |
| `uuids_only` | query | `boolean` | no | Return production UUIDs only. |
