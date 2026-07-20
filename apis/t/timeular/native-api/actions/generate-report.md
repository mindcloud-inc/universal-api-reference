# Generate Report with Timeular

Generates a time entry report in your Timeular workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/report`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Generate Report](https://developers.early.app/#04fcb4f6-7a83-4117-91dc-1e9ab75b0519)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activities` | body | `string` | no |
| `date` | body | `string` | yes |
| `fileType` | body | `string` | yes |
| `folders` | body | `string` | no |
| `mentions` | body | `string` | no |
| `noteQuery` | body | `string` | no |
| `operator` | body | `string` | no |
| `tags` | body | `string` | no |
| `users` | body | `string` | no |
