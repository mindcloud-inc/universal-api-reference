# Show Map At Zoom Level with Waze Deep Links

Generates a Waze map URL for a zoom level.

## Endpoint

- **Method:** `GET`
- **Path:** `https://waze.com/ul`
- **Base URL:** `https://waze.com/ul`
- **Official documentation:** [Show Map At Zoom Level](https://developers.google.com/waze/deeplinks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `z` | query | `number` | yes | Map magnification level from 6 to 8192. |
