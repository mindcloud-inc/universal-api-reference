# List Recordings with Basecamp

Retrieves recordings from Basecamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/projects/recordings.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [List Recordings](https://github.com/basecamp/bc3-api/blob/master/sections/recordings.md#get-recordings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Basecamp account ID. |
| `type` | query | `list<string>` | yes | Recording type to list. Accepted values: `Comment`, `Document`, `Kanban::Card`, `Kanban::Step`, `Message`, `Question::Answer`, `Schedule::Entry`, `Todo`, `Todolist`, `Upload`, `Vault`. |
| `bucket` | query | `string` | no | Single or comma-separated list of project IDs. Send multiple values as a string separated by `,`. |
| `status` | query | `list<string>` | no | Recording status. Accepted values: `active`, `archived`, `trashed`. |
| `sort` | query | `list<string>` | no | Sort field. Accepted values: `created_at`, `updated_at`. |
| `direction` | query | `list<string>` | no | Sort direction. Accepted values: `asc`, `desc`. |
