# Unarchive Incident by ID with TOPdesk

Unarchives an incident in TOPdesk by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/incidents/id/:id/unarchive`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Unarchive Incident by ID](https://developers.topdesk.com/explorer/?page=incident)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Incident identifier. |
| `unarchive_partials` | query | `boolean` | no | Whether linked partial incidents should be unarchived as well. |
