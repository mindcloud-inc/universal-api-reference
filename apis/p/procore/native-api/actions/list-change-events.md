# List Change Events with Procore

Retrieves change events from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.1/change_events`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Change Events](https://developers.procore.com/reference/rest/change-events#list-change-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | Unique identifier for the project. |
