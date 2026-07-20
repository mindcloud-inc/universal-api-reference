# Archive Incident by ID with TOPdesk

Archives an incident in TOPdesk by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/incidents/id/:id/archive`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Archive Incident by ID](https://developers.topdesk.com/explorer/?page=incident)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Incident identifier. |
| `id` | body | `string` | no | Archiving reason id (UUID). |
| `name` | body | `string` | no | Archiving reason name when id is not provided. |
