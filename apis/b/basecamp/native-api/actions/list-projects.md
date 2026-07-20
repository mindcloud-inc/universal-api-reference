# List Projects with Basecamp

Retrieves all visible projects from Basecamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/projects.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [List Projects](https://github.com/basecamp/bc3-api/blob/master/sections/projects.md#get-all-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID from List Authorized Accounts (numeric segment of the `bc3` `href`) |
| `status` | query | `list<string>` | no | active, archived, or trashed Accepted values: `archived`, `trashed`. |
