# Create Service with Makeplans

Creates a new service in Makeplans.

## Endpoint

- **Method:** `POST`
- **Path:** `/services`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Create Service](https://developer.makeplans.com/endpoints/services/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service.booking_type` | body | `list` | no | Service booking type. Use Attendance / Event when creating services for events/classes. Accepted values: `0`, `1`, `2`, `3`. |
| `service.title` | body | `string` | yes | Service title. |
| `service.interval` | body | `number` | no | Service interval in minutes. |
