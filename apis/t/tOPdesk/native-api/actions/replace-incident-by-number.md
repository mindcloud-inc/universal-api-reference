# Replace Incident by Number with TOPdesk

Replaces an existing incident in TOPdesk by number.

## Endpoint

- **Method:** `PUT`
- **Path:** `/incidents/number/:number`
- **Base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`
- **Official documentation:** [Replace Incident by Number](https://developers.topdesk.com/explorer/?page=incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `briefDescription` | body | `string` | no | Updated short incident summary. |
| `number` | path | `string` | yes | Incident number. |
