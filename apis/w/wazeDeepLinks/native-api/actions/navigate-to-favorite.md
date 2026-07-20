# Navigate To Favorite with Waze Deep Links

Generates a Waze navigation URL to a saved favorite.

## Endpoint

- **Method:** `GET`
- **Path:** `https://waze.com/ul`
- **Base URL:** `https://waze.com/ul`
- **Official documentation:** [Navigate To Favorite](https://developers.google.com/waze/deeplinks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `favorite` | query | `list` | yes | Saved Waze favorite destination. Accepted values: `Home`, `Work`. |
