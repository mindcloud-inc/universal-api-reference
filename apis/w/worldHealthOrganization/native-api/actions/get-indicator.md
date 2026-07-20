# Get Indicator with World Health Organization

Retrieves an indicator from the World Health Organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/Indicator(':indicatorCode')`
- **Base URL:** `https://ghoapi.azureedge.net/api/`
- **Official documentation:** [Get Indicator](https://www.who.int/data/gho/info/gho-odata-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indicatorCode` | path | `string` | yes | WHO indicator code, such as WHOSIS_000001. |
