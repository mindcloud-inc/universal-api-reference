# Send Structure Run Event with Griptape

Sends a structure run event to Griptape.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/structure-runs/:structure_run_id/events`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Send Structure Run Event](https://docs.griptape.ai/stable/griptape-cloud/structures/structure-run-events/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `structure_run_id` | path | `string` | yes | The structure run ID to publish events to. |
| `payload` | body | `object` | yes | Event payload object to publish into the Structure Run event stream. |
| `type` | body | `string` | no | Optional event type. Griptape defaults this to UserEvent when omitted. |
| `timestamp` | body | `number` | no | Optional UNIX timestamp for the event. If omitted, Griptape sets the current time. |
