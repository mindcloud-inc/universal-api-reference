# List Checkpad Events with MOONTO Shopping Lists - Checkpad

Retrieves checkpad event records from Checkpad.

## Endpoint

- **Method:** `GET`
- **Path:** `/checkpads/{checkpad_id}/events`
- **Base URL:** `https://api.moonto.app`
- **Official documentation:** [List Checkpad Events](https://api.moonto.app/docs#/Checkpads/get_checkpad_events_checkpads__checkpad_id__events_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkpad_id` | path | `string` | yes | The ID of the MOONTO checkpad whose events should be returned. |
