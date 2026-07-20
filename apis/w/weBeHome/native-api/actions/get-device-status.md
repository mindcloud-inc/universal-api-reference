# Get Device Status with WeBeHome

## Endpoint

- **Method:** `GET`
- **Path:** `WebAPI.aspx`
- **Base URL:** `https://webehome.com/API`
- **Official documentation:** [Get Device Status](https://www.webehome.com/Doc/WBH_Customer_API.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BaseUnitID` | query | `string` | yes | Base unit ID. Leave empty to search all accessible base units. |
| `SubUnitID` | query | `string` | no | Optional sub unit ID to return one device only. |
