# Reorder All Collections with Raindrop

## Endpoint

- **Method:** `PUT`
- **Path:** `/collections`
- **Base URL:** `https://api.raindrop.io/rest/v1`
- **Official documentation:** [Reorder All Collections](https://developer.raindrop.io/v1/collections/methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | body | `string` | yes | Order applied to all collections. Allowed values: title, -title, -count. |
