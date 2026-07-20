# Remove Multiple Collections with Raindrop

## Endpoint

- **Method:** `DELETE`
- **Path:** `/collections`
- **Base URL:** `https://api.raindrop.io/rest/v1`
- **Official documentation:** [Remove Multiple Collections](https://developer.raindrop.io/v1/collections/methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Array of collection IDs to remove. |
