# List Incident Requests with TOPdesk

Retrieves requests for an incident from TOPdesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents/id/:id/requests`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [List Incident Requests](https://developers.topdesk.com/explorer/?page=incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Incident identifier. |
