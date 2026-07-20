# List Vehicle Battery History with Zubie

Retrieves vehicle battery history from Zubie.

## Endpoint

- **Method:** `GET`
- **Path:** `/vehicle/{vehicle_key}/battery-history`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [List Vehicle Battery History](https://developer.zubie.com/reference/vehicles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vehicle_key` | path | `string` | yes | Unique vehicle key. |
