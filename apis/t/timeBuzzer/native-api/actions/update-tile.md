# Update Tile with timeBuzzer

## Endpoint

- **Method:** `PUT`
- **Path:** `/open-api/tiles/:id`
- **Base URL:** `https://my.timebuzzer.com`
- **Official documentation:** [Update Tile](https://my.timebuzzer.com/doc/#api-Tiles-EditTile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The tile ID. |
| `name` | body | `string` | yes | The tile name. |
| `parents[]` | body | `array<number>` | no | The parent tile IDs. Send multiple values as a array. |
| `archived` | body | `boolean` | no | Whether the tile is archived. |
| `type` | body | `string` | yes | The tile type. |
| `layer` | body | `number` | yes | The layer ID. |
| `favorite` | body | `boolean` | no | Whether the tile is a favorite. |
| `color` | body | `string` | no | The tile color. |
| `description` | body | `string` | no | The tile description. |
| `customData` | body | `string` | no | Custom tile data. |
