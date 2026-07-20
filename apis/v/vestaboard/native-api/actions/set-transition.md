# Set Transition with Vestaboard

Updates transition settings in Vestaboard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/transition`
- **Base URL:** `https://cloud.vestaboard.com`
- **Official documentation:** [Set Transition](https://docs.vestaboard.com/docs/read-write-api/endpoints/#set-transition)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transition` | body | `list` | yes | Transition style to apply. Accepted values: `classic`, `curtain`, `drift`, `wave`. |
| `transitionSpeed` | body | `list` | yes | Transition speed to apply. Accepted values: `fast`, `gentle`. |
