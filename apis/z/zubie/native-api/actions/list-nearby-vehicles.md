# List Nearby Vehicles with Zubie

Retrieves nearby vehicles from Zubie.

## Endpoint

- **Method:** `GET`
- **Path:** `/vehicles/nearby`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [List Nearby Vehicles](https://developer.zubie.com/reference/vehicles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `string` | yes | Latitude of the point. |
| `lot` | query | `string` | yes | Longitude of the point. |
