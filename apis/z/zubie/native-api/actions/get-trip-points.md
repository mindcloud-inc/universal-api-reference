# Get Trip Points with Zubie

Retrieves trip points from Zubie.

## Endpoint

- **Method:** `GET`
- **Path:** `/trip/{trip_key}/points`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [Get Trip Points](https://developer.zubie.com/reference/trips)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trip_key` | path | `string` | yes | Unique trip key. |
