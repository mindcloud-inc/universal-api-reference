# Create a status update with Asana

Creates a status update in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `status_updates`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a status update](https://developers.asana.com/reference/createstatusforobject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no |
| `data` | body | `object` | yes |
