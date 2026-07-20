# Update Incident by ID (Patch) with TOPdesk

Updates an incident in TOPdesk by ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/incidents/id/:id`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Update Incident by ID (Patch)](https://developers.topdesk.com/explorer/?page=incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `briefDescription` | body | `string` | no | Updated short incident summary. |
| `id` | path | `string` | yes | Incident identifier. |
