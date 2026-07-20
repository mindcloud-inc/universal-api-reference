# Create Tile with timeBuzzer

## Endpoint

- **Method:** `POST`
- **Path:** `/open-api/tiles`
- **Base URL:** `https://my.timebuzzer.com`
- **Official documentation:** [Create Tile](https://my.timebuzzer.com/doc/#api-Tiles-CreateTile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tile name. |
| `parents[]` | body | `array<number>` | no | Optional parent tile IDs. |
| `archived` | body | `boolean` | no | Whether the tile is archived. |
| `type` | body | `string` | yes | Tile type. |
| `layer` | body | `number` | yes | Layer ID for the tile. |
| `favorite` | body | `boolean` | no | Whether the tile is a favorite. |
| `color` | body | `string` | no | ARGB color hex for the tile. |
| `description` | body | `string` | no | Optional tile description. |
| `customData` | body | `string` | no | Optional custom data string. |
