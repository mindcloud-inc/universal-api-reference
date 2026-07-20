# Import Leads with RoboAuditor

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/import`
- **Base URL:** `https://app.siteauditor.com/api`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | CSV file content/form-data for bulk lead import. |
