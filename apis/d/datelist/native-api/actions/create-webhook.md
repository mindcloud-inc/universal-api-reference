# Create Webhook with Datelist

Creates a new webhook in Datelist for booking notifications.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://datelist.io/api`
- **Official documentation:** [Create Webhook](https://apidoc.datelist.io/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL Datelist should call for new booking notifications. |
| `calendar_id` | body | `number` | yes | The Datelist calendar to watch for new bookings. |
