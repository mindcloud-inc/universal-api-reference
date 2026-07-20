# Trigger Events (Bulk) with Sequenzy

Triggers events for multiple subscribers in Sequenzy.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/events/bulk`
- **Base URL:** `https://api.sequenzy.com/api/v1`
- **Official documentation:** [Trigger Events (Bulk)](https://docs.sequenzy.com/api-reference/subscribers/events/trigger-bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Subscriber email address. |
| `events` | body | `list<object>` | yes | Events to trigger in bulk. |
