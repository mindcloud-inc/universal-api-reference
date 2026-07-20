# Create Event Listener with mintBlue

Creates a new event listener in mintBlue.

## Endpoint

- **Method:** `POST`
- **Path:** `/sdk/latest`
- **Base URL:** `https://api.mintblue.com`
- **Official documentation:** [Create Event Listener](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#createEventListener)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.name` | body | `string` | yes | Event listener name. |
| `params.trigger.type` | body | `string` | yes | Trigger type. |
| `params.trigger.options` | body | `object` | yes | Trigger options object. For `mintblue.transaction.created`, include `project_id` and `txo`. |
| `params.actions[]` | body | `array<object>` | yes | Action definitions array. Use provider token `insert_into_project` (underscore) or `webhook`. |
