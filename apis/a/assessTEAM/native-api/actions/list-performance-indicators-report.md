# List Performance Indicators Report with AssessTEAM

Retrieves the performance indicators report from AssessTEAM.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/performanceindicators`
- **Base URL:** `https://restapi.assessteam.com`
- **Official documentation:** [List Performance Indicators Report](https://restapi.assessteam.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromdate` | query | `string` | yes | From month of the date range, for example Jan-2026. |
| `todate` | query | `string` | yes | To month of the date range, for example Apr-2026. |
| `resultareaname` | query | `string` | no | Result area name, for example Engineering. |
| `display` | query | `string` | no | Display mode, 1 for scores by evaluation or 2 for average scores by peer level. |
| `projectname` | query | `string` | no | Project name, for example Acme web site. |
| `teamname` | query | `string` | no | Team name, for example Testing team. |
| `personname` | query | `string` | no | Person name, for example Jon doe. |
| `peer` | query | `boolean` | no | Include evaluations from peer reviews. |
| `upward` | query | `boolean` | no | Include evaluations from upward reviews. |
| `self` | query | `boolean` | no | Include evaluations from self reviews. |
| `downward` | query | `boolean` | no | Include evaluations from downward reviews. |
| `customer` | query | `boolean` | no | Include customer satisfaction evaluations. |
| `undefined` | query | `boolean` | no | Include undefined evaluation levels. |
