# Send Flow To Contact with Fliqr AI

Sends a flow to a contact in Fliqr AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:user_id/send/:flow_id`
- **Base URL:** `https://app.fliqr.ai/api/`
- **Official documentation:** [Send Flow To Contact](https://docs.fliqr.ai/api-reference/users/post-users-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | Fliqr contact user ID. |
| `flow_id` | path | `number` | yes | Flow ID to send. |
