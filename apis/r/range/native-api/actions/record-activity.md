# Record Activity with Range

Record an activity interaction for a user with attachment data.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/activity`
- **Base URL:** `https://api.range.co`
- **Official documentation:** [Record Activity](https://www.range.co/docs/api#rpc-record-interaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment` | body | `object` | no | Attachment object to upsert with the interaction. |
| `attachment_id` | body | `string` | no | Existing attachment ID to associate with the interaction. |
| `idempotency_key` | body | `string` | no | Optional de-duplication key. |
| `interaction_at` | body | `string` | no | Timestamp when the interaction occurred. |
| `interaction_type` | body | `number` | no | The interaction type enum value. |
| `user_id` | body | `string` | no | The user who should receive the activity. |
