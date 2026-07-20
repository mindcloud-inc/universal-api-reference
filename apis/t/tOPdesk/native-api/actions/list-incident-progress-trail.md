# List Incident Progress Trail with TOPdesk

Retrieves the progress trail for an incident from TOPdesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents/id/:id/progresstrail`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [List Incident Progress Trail](https://developers.topdesk.com/explorer/?page=incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Incident identifier. |
