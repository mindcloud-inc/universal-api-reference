# Get Incident Time Spent with TOPdesk

Retrieves time spent for an incident from TOPdesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents/id/:id/timespent`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Get Incident Time Spent](https://developers.topdesk.com/explorer/?page=incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Incident identifier. |
