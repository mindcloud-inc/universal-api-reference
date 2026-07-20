# List Persons Report with AssessTEAM

Retrieves the persons report from AssessTEAM.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/persons`
- **Base URL:** `https://restapi.assessteam.com`
- **Official documentation:** [List Persons Report](https://restapi.assessteam.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromdate` | query | `string` | yes | From month of the date range, for example Jan-2026. |
| `todate` | query | `string` | yes | To month of the date range, for example Apr-2026. |
| `display` | query | `string` | no | Display mode, for example 3. |
| `projectname` | query | `string` | no | Project name, for example Acme Web Site. |
| `teamname` | query | `string` | no | Team name, for example Testing Team. |
| `personname` | query | `string` | no | Person name, for example Jon Doe. |
| `peer` | query | `boolean` | no | Include peer evaluations. |
| `upward` | query | `boolean` | no | Include upward evaluations. |
| `self` | query | `boolean` | no | Include self evaluations. |
| `downward` | query | `boolean` | no | Include downward evaluations. |
| `customer` | query | `boolean` | no | Include customer evaluations. |
| `undefined` | query | `boolean` | no | Include undefined evaluation level. |
