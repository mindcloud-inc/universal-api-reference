# Search Tiles with timeBuzzer

## Endpoint

- **Method:** `POST`
- **Path:** `/open-api/tiles/filters`
- **Base URL:** `https://my.timebuzzer.com`
- **Official documentation:** [Search Tiles](https://my.timebuzzer.com/doc/#api-Tiles-GetFilteredTiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional tile name filter. |
| `archived` | body | `boolean` | no | Whether to return archived tiles. |
| `layers[]` | body | `array<number>` | no | Optional layer IDs to filter by. |
