# List Time Offs with OfficeClip

Retrieves time off entries from OfficeClip.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/timeoff-summary`
- **Base URL:** `https://app.officeclip.com`
- **Official documentation:** [List Time Offs](https://app.officeclip.com/swagger/ui/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | yes | Required OfficeClip category such as mylist, inbox, or archived. |
