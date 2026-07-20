# Create Event with Makeplans

Creates a new event in Makeplans.

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Create Event](https://developer.makeplans.com/endpoints/events/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event.resource_id` | body | `number` | yes | Required Makeplans resource ID. |
| `event.title` | body | `string` | no | Optional event title. |
| `event.service_id` | body | `number` | yes | Required Makeplans service ID. |
| `event.capacity` | body | `number` | yes | Required event capacity. |
| `event.starts_at` | body | `date` | yes | Event start datetime. |
| `event.ends_at` | body | `date` | yes | Event end datetime. |
