# Add Incident Time Spent with TOPdesk

Creates a time spent entry for an incident in TOPdesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/incidents/id/:id/timespent`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Add Incident Time Spent](https://developers.topdesk.com/explorer/?page=incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Incident identifier. |
| `notes` | body | `string` | no | Optional note for time registration. |
| `timeSpent` | body | `number` | yes | Time spent in minutes. |
