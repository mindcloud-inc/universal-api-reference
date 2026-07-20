# Get COD Coverage Area with iPaymu

Check whether a location is covered by iPaymu cash-on-delivery service.

## Endpoint

- **Method:** `GET`
- **Path:** `/cod/area`
- **Base URL:** `https://my.ipaymu.com/api/v2`
- **Official documentation:** [Get COD Coverage Area](https://ipaymu.com/api-collection/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `area` | query | `string` | yes | Area search text with at least three characters. |
