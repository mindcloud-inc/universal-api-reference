# Create Event with Schedule It

Creates a new event in Schedule It.

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://www.scheduleit.com/api`
- **Official documentation:** [Create Event](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The event title. |
| `owner` | body | `number` | yes | Resource ID to tag as the event owner. |
| `date_start` | body | `string` | yes | The event start date and time. |
| `date_end` | body | `string` | yes | The event end date and time. |
| `notes` | body | `string` | no | Notes for the event. |
