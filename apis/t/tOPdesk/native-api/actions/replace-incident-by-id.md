# Replace Incident by ID with TOPdesk

Replaces an existing incident in TOPdesk by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/incidents/id/:id`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Replace Incident by ID](https://developers.topdesk.com/explorer/?page=incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `briefDescription` | body | `string` | no | Updated short incident summary. |
| `id` | path | `string` | yes | Incident identifier. |
