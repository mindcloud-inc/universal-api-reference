# Get events on a resource with Asana

Retrieves events for a resource from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `events`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get events on a resource](https://developers.asana.com/reference/getevents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no |
| `resource` | query | `string` | yes |
