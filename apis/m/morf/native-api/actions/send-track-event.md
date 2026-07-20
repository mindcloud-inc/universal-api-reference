# Send Track Event with Morf

Sends a track event to Morf.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{trackWebhookUrl}`
- **Official documentation:** [Send Track Event](https://www.morf.health/docs/events/payloads/morf/track)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_name` | body | `string` | yes | Name of the Track event to send to Morf. |
| `user_id` | body | `string` | yes | Unique user ID for the Track event. Morf stores this as the active customer ID. |
| `event_id` | body | `string` | no | Optional unique identifier for the Track event. |
| `occurred_at` | body | `date` | no | Optional event time in RFC3339 ISO format. |
| `profile_ids` | body | `object` | no | Optional third-party IDs to associate with the Morf Profile. |
| `profile_properties` | body | `object` | no | Optional property values to store on the Morf Profile. |
| `event_data` | body | `object` | no | Optional data associated with the event for Morf Workflows. |
