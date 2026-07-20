# Create a monitor for a business with Middesk

Creates a business monitor in Middesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses/:business_id/monitor`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create a monitor for a business](https://docs.middesk.com/reference/businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business to create a monitor for. |
| `event_types[]` | body | `array` | yes | Event types to monitor for the business. |
