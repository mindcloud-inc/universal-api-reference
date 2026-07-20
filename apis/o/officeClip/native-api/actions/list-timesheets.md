# List Timesheets with OfficeClip

Retrieves timesheets from OfficeClip.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/timesheet-summary`
- **Base URL:** `https://app.officeclip.com`
- **Official documentation:** [List Timesheets](https://app.officeclip.com/swagger/ui/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | yes | Required OfficeClip category such as inbox, outbox, or archived. |
