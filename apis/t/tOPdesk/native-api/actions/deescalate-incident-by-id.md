# Deescalate Incident by ID with TOPdesk

Deescalates an incident in TOPdesk by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/incidents/id/:id/deescalate`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Deescalate Incident by ID](https://developers.topdesk.com/explorer/?page=incident)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Incident identifier. |
| `id` | body | `string` | no | Deescalation reason id (UUID). |
| `name` | body | `string` | no | Deescalation reason name when id is not provided. |
