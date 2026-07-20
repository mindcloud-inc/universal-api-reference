# Set Switch Status with WeBeHome

## Endpoint

- **Method:** `GET`
- **Path:** `WebAPI.aspx`
- **Base URL:** `https://webehome.com/API`
- **Official documentation:** [Set Switch Status](https://www.webehome.com/Doc/WBH_Customer_API.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BaseUnitID` | query | `string` | yes | Base unit ID. |
| `SubUnitID` | query | `string` | yes | Sub unit ID. |
| `Status` | query | `string` | yes | 0=off, 1-98 dim level, 99=on. |
