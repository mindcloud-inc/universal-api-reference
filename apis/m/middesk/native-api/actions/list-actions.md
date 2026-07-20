# List actions for an object with Middesk

Retrieves actions for an object from Middesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/actions`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [List actions for an object](https://docs.middesk.com/reference/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_id` | query | `string` | yes | ID of the object whose actions you want to list. |
| `object_type` | query | `string` | yes | Type of object whose actions you want to list. |
