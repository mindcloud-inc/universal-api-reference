# Retrieve an action with Middesk

Retrieves an action from your Middesk account.

## Endpoint

- **Method:** `GET`
- **Path:** `/actions/:id`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Retrieve an action](https://docs.middesk.com/reference/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the action to retrieve. |
| `object_id` | query | `string` | yes | ID of the object associated with the action. |
| `object_type` | query | `string` | yes | Type of object associated with the action. |
