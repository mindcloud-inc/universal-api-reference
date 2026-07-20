# Update Place with Zubie

Updates an existing place in Zubie.

## Endpoint

- **Method:** `POST`
- **Path:** `/place/{place_key}`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [Update Place](https://developer.zubie.com/reference/places)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_time` | body | `string` | yes | Start time window in hh:mm format. |
| `place_key` | path | `string` | yes | Unique place key. |
| `to_time` | body | `string` | yes | End time window in hh:mm format. |
