# Bulk Import Time Entries with Timely

Creates a bulk import job for time entries in Timely.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.1/{account_id}/bulk/hours`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Bulk Import Time Entries](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Workspace id |
| `create[]` | body | `array<object>` | no | Array of time entries to create. Each item accepts all standard event/time entry fields from PayloadSchema. |
| `update[]` | body | `array<object>` | no | Array of time entries to update. Must include id field. All other fields from UpdatePayloadSchema are optional. |
| `delete[]` | body | `array<number>` | no | Array of time entry IDs to delete |
