# List Incident Actions with TOPdesk

Retrieves actions for an incident from TOPdesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents/id/:id/actions`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [List Incident Actions](https://developers.topdesk.com/explorer/?page=incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Incident identifier. |
