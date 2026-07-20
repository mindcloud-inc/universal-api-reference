# Create Webhook with OnceHub

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks`
- **Base URL:** `https://api.oncehub.com`
- **Official documentation:** [Create Webhook](https://developers.oncehub.com/reference/oncehub-v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Unique name for the webhook subscription. |
| `url` | body | `string` | yes | Full HTTPS endpoint OnceHub should call when subscribed events occur. |
| `events` | body | `list<string>` | yes | Event types that should trigger the webhook subscription. Accepted values: `booking`, `booking.canceled`, `booking.canceled_reschedule_requested`, `booking.canceled_then_rescheduled`, `booking.completed`, `booking.no_show`, `booking.rescheduled`, `booking.scheduled`, `conversation`, `conversation.abandoned`, `conversation.closed`, `conversation.started`. Send multiple values as a array. |
