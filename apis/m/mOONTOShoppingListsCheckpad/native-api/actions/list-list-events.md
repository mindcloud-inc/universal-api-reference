# List List Events with MOONTO Shopping Lists - Checkpad

Retrieves shopping list events from Checkpad.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/{list_id}/events`
- **Base URL:** `https://api.moonto.app`
- **Official documentation:** [List List Events](https://api.moonto.app/docs#/Lists/get_list_events_lists__list_id__events_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The ID of the MOONTO list whose events should be returned. |
