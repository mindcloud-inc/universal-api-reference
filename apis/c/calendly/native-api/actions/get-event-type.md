# Get Event Type with Calendly

Retrieves an event type from Calendly.

## Endpoint

- **Method:** `GET`
- **Path:** `/event_types/:event_type_uuid`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Get Event Type](https://developer.calendly.com/how-to-get-scheduling-page-links-for-team-members-across-the-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type_uuid` | path | `string` | yes | Event type UUID from Calendly. |
