# Create Event with Circle

Creates a new event in Circle.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/v2/events`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Create Event](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `object` | yes | Event payload object |
| `space_id` | body | `list<number>` | yes | Space ID for the event |
