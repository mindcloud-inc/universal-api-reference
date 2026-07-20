# Trigger Event with Sequenzy

Triggers an event for a subscriber in Sequenzy.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/events`
- **Base URL:** `https://api.sequenzy.com/api/v1`
- **Official documentation:** [Trigger Event](https://docs.sequenzy.com/api-reference/subscribers/events/trigger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Subscriber email address. |
| `event` | body | `string` | yes | Event name. |
