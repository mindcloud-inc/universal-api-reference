# Identify Color By CMYK with The Color

Identifies a color in The Color by CMYK value.

## Endpoint

- **Method:** `GET`
- **Path:** `/id`
- **Base URL:** `https://www.thecolorapi.com`
- **Official documentation:** [Identify Color By CMYK](https://www.thecolorapi.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cmyk` | query | `string` | yes | Valid CMYK color, such as 100,58,0,33 or cmyk(100,58,0,33). |
