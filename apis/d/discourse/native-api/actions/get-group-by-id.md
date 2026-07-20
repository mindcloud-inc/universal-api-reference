# Get Group By Id with Discourse

Retrieves a Discourse group by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/by-id/:id.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Get Group By Id](https://docs.discourse.org/#tag/Groups/operation/getGroupById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Group ID or group name accepted by Discourse. |
