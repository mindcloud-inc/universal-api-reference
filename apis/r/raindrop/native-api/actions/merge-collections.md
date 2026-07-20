# Merge Collections with Raindrop

## Endpoint

- **Method:** `PUT`
- **Path:** `/collections/merge`
- **Base URL:** `https://api.raindrop.io/rest/v1`
- **Official documentation:** [Merge Collections](https://developer.raindrop.io/v1/collections/methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Array of collection IDs to merge from. |
| `to` | body | `number` | yes | Collection ID to merge into. |
