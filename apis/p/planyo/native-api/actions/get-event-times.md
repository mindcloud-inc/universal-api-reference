# Get Event Times with Planyo

Retrieves event times from Planyo.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Get Event Times](https://www.planyo.com/api.php?topic=get_event_times)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `resource_id` | query | `number` | yes |
| `format` | query | `string` | no |
| `future_only` | query | `boolean` | no |
