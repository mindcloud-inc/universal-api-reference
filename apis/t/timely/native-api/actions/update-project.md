# Update Project with Timely

Updates an existing project in Timely.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1.1/{account_id}/projects/{id}`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Update Project](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `id` | path | `number` | yes | Project ID |
| `project` | body | `object` | yes | — |
