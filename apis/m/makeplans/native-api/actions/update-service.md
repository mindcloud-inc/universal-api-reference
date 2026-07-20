# Update Service with Makeplans

Updates an existing service in Makeplans.

## Endpoint

- **Method:** `PUT`
- **Path:** `/services/:serviceId`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Update Service](https://developer.makeplans.com/endpoints/services/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service.booking_type` | body | `list` | no | Service booking type. Use Attendance / Event when updating a service for events/classes. Accepted values: `0`, `1`, `2`, `3`. |
| `service.interval` | body | `number` | no | Service interval in minutes. |
| `service.title` | body | `string` | no | Service title. |
| `serviceId` | path | `number` | yes | The Makeplans service ID. |
