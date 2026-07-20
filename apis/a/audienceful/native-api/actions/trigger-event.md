# Trigger Event with Audienceful

Triggers Audienceful automations by event name.

## Endpoint

- **Method:** `POST`
- **Path:** `/automations/event/`
- **Base URL:** `https://app.audienceful.com/api`
- **Official documentation:** [Trigger Event](https://developer.audienceful.com/api-reference/automations/event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | The event name to trigger. |
| `email` | body | `string` | yes | The person's email. |
| `event_properties` | body | `object` | no | Event property payload used in automations. |
| `fields` | body | `object` | no | Field values to merge onto the person before the event runs. |
