# Create Change Event with Procore

Creates a new change event in Procore.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v1.1/change_events`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [Create Change Event](https://developers.procore.com/reference/rest/change-events#create-change-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `change_event` | body | `object` | yes | Change event payload object. |
| `project_id` | query | `string` | yes | Unique identifier for the project. |
