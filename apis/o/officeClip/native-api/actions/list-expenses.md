# List Expenses with OfficeClip

Retrieves expenses from OfficeClip.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/expense-summary`
- **Base URL:** `https://app.officeclip.com`
- **Official documentation:** [List Expenses](https://app.officeclip.com/swagger/ui/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | yes | Required OfficeClip category such as inbox, outbox, or archived. |
