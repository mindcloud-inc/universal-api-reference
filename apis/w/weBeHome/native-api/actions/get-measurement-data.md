# Get Measurement Data with WeBeHome

## Endpoint

- **Method:** `GET`
- **Path:** `WebAPI.aspx`
- **Base URL:** `https://webehome.com/API`
- **Official documentation:** [Get Measurement Data](https://www.webehome.com/Doc/WBH_Customer_API.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SubUnitID` | query | `string` | no | One ID, a comma-separated list of IDs, or empty. |
| `BaseUnitID` | query | `string` | yes | Base unit ID. |
| `FromDT` | query | `string` | yes | Start date in yyyy-mm-dd. Empty means the last 7 days. |
