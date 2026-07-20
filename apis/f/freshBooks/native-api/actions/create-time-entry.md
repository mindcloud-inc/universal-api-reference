# Create Time Entry with FreshBooks

Creates a new time entry in FreshBooks for a business.

## Endpoint

- **Method:** `POST`
- **Path:** `/timetracking/business/:businessId/time_entries`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Create Time Entry](https://www.freshbooks.com/api/time_entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | FreshBooks business ID. |
| `timeEntry.duration` | body | `number` | yes | Duration in seconds. |
| `timeEntry.started_at` | body | `string` | yes | Start timestamp. |
| `timeEntry.identity_id` | body | `number` | yes | FreshBooks identity ID. |
| `timeEntry.client_id` | body | `number` | no | FreshBooks client ID. |
| `timeEntry.project_id` | body | `number` | no | FreshBooks project ID. |
| `timeEntry.is_logged` | body | `boolean` | yes | Whether the entry is logged. |
| `timeEntry.note` | body | `string` | no | Time entry note. |
