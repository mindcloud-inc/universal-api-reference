# Create Event with SavvyCal

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/links/:link_id/events`
- **Base URL:** `https://api.savvycal.com`
- **Official documentation:** [Create Event](https://developers.savvycal.com/api/create-event)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `link_id` | path | `string` | yes |
| `display_name` | body | `string` | yes |
| `email` | body | `string` | yes |
| `start_at` | body | `date` | yes |
| `end_at` | body | `date` | yes |
| `time_zone` | body | `string` | yes |
| `phone_number` | body | `string` | no |
| `fields[]` | body | `array<object>` | no |
| `metadata` | body | `object` | no |
