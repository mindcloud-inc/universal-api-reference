# List Announcements with Instructure

Retrieves announcements from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/announcements`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [List Announcements](https://developerdocs.instructure.com/services/canvas/resources/announcements#method.announcements_api.index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `context_codes[]` | query | `string` | yes | One or more Canvas context codes such as course_123. Send multiple values as a array. |
