# Search Amenities with Caltrain

Finds Caltrain amenities within map bounds.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/amenities/:west,:south,:east,:north`
- **Base URL:** `https://www.caltrain.com`
- **Official documentation:** [Search Amenities](https://www.caltrain.com/developer-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `west` | path | `number` | yes | West longitude bound. |
| `south` | path | `number` | yes | South latitude bound. |
| `east` | path | `number` | yes | East longitude bound. |
| `north` | path | `number` | yes | North latitude bound. |
