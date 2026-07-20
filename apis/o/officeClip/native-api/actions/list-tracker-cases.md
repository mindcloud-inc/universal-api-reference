# List Tracker Cases with OfficeClip

Retrieves tracker cases from OfficeClip.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/tracker-case-summary`
- **Base URL:** `https://app.officeclip.com`
- **Official documentation:** [List Tracker Cases](https://app.officeclip.com/swagger/ui/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `binderSid` | query | `string` | yes | Required OfficeClip tracker binder id. |
