# Update a monitor for a business with Middesk

Updates a business monitor in Middesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/businesses/:business_id/monitor`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Update a monitor for a business](https://docs.middesk.com/reference/businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business whose monitor you want to update. |
| `event_types[]` | body | `array` | yes | Event types to monitor for the business. |
