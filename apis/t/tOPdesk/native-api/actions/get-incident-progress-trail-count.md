# Get Incident Progress Trail Count with TOPdesk

Retrieves an incident progress trail count from TOPdesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents/id/:id/progresstrail/count`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Get Incident Progress Trail Count](https://developers.topdesk.com/explorer/?page=incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Incident identifier. |
