# List Events with ProProfs Project

Retrieves a list of events from ProProfs Project.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [List Events](https://help.proprofsproject.com/events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `due_date_from` | query | `string` | no | Filter events with a due date on or after this date. |
| `due_date_to` | query | `string` | no | Filter events with a due date on or before this date. |
| `limit` | query | `string` | no | Limit the number of returned events. |
| `offset` | query | `string` | no | Offset for returned events. |
| `project_id` | query | `string` | no | Filter events by project ID. |
