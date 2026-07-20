# Update Incident by Number (Patch) with TOPdesk

Updates an incident in TOPdesk by number.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/incidents/number/:number`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Update Incident by Number (Patch)](https://developers.topdesk.com/explorer/?page=incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `briefDescription` | body | `string` | no | Updated short incident summary. |
| `number` | path | `string` | yes | Incident number. |
