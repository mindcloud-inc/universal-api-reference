# List Projects with Timely

Retrieves projects from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/projects`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [List Projects](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID for the clients you want to retrieve |
| `offset` | query | `number` | no | Retrieve projects from offset |
| `limit` | query | `number` | no | Retrieve number of projects |
| `order` | query | `string` | no | Sorting order - desc, asc (Default desc) |
| `filter` | query | `string` | no | Deprecated: Filter projects - mine, active, archived, all (Default mine, ignored if state or relation parameter present) |
| `state` | query | `string` | no | Filter projects - active, archived, all |
| `relation` | query | `string` | no | Filter projects - assigned, created, all |
| `updated_after` | query | `string` | no | Retrieve records updated after a certain timestamp |
| `project_ids[]` | query | `array<number>` | no | Retrieve specific projects |
| `external_ids[]` | query | `array<number>` | no | Retrieve specific projects by external ID reference |
