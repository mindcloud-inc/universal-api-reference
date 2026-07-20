# Update Project with CompanyCam

## Endpoint

- **Method:** `PUT`
- **Path:** `projects/:id`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Update Project](https://docs.companycam.com/reference/updateproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address.street_address_1` | body | `string` | no | — |
| `coordinates.lat` | body | `number` | no | — |
| `id` | path | `string` | yes | Project Id |
| `name` | body | `string` | no | — |
| `address` | body | `object` | no | — |
| `address.street_address_2` | body | `string` | no | — |
| `coordinates.lon` | body | `number` | no | — |
| `geofence[].lat` | body | `number` | no | — |
| `address.city` | body | `string` | no | — |
| `coordinates` | body | `object` | no | — |
| `geofence[].lon` | body | `number` | no | — |
| `address.state` | body | `string` | no | — |
| `geofence[]` | body | `array<object>` | no | — |
| `address.postal_code` | body | `string` | no | — |
| `address.country` | body | `string` | no | — |
