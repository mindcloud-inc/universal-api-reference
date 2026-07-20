# Get Event Data with WeBeHome

## Endpoint

- **Method:** `GET`
- **Path:** `WebAPI.aspx`
- **Base URL:** `https://webehome.com/API`
- **Official documentation:** [Get Event Data](https://www.webehome.com/Doc/WBH_Customer_API.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BaseUnitID` | query | `string` | yes | Base unit ID. Leave empty to search all accessible base units. |
| `LastDataID` | query | `string` | yes | Start returning rows after this data ID. Empty means the last 24 hours. |
