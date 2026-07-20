# Create an action on an object with Middesk

Creates an action on an object in Middesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create an action on an object](https://docs.middesk.com/reference/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_id` | body | `string` | yes | ID of the object to create the action on. |
| `object_type` | body | `string` | yes | Type of object to create the action on. |
| `payload` | body | `object` | yes | Payload for the requested action. |
| `type` | body | `string` | yes | Action type to create. |
