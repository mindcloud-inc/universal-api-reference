# Escalate Incident by ID with TOPdesk

Escalates an incident in TOPdesk by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/incidents/id/:id/escalate`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Escalate Incident by ID](https://developers.topdesk.com/explorer/?page=incident)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Incident identifier. |
| `id` | body | `string` | no | Escalation reason id (UUID). |
| `name` | body | `string` | no | Escalation reason name when id is not provided. |
