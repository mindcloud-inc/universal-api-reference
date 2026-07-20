# Create Incident with TOPdesk

Creates a new incident in TOPdesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/incidents`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Create Incident](https://developers.topdesk.com/explorer/?page=incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `briefDescription` | body | `string` | yes | Short incident summary. |
| `caller.id` | body | `string` | yes | Registered caller person id (UUID). |
| `request` | body | `string` | no | Initial incident request text. |
