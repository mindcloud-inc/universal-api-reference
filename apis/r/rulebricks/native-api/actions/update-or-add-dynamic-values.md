# Update or Add Dynamic Values with Rulebricks

Updates or adds dynamic values in Rulebricks.

## Endpoint

- **Method:** `POST`
- **Path:** `/values`
- **Base URL:** `https://rulebricks.com/api/v1`
- **Official documentation:** [Update or Add Dynamic Values](https://rulebricks.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_groups[]` | body | `array<string>` | no | Optional array of user group names or IDs |
| `values` | body | `object` | yes | Dictionary of keys and values to update or add |
