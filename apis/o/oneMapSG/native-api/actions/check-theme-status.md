# Check Theme Status with OneMap SG

Retrieves the status of a OneMap SG theme.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/themesvc/checkThemeStatus`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Check Theme Status](https://www.onemap.gov.sg/apidocs/themes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queryName` | query | `string` | yes | The theme query name. |
| `dateTime` | query | `string` | yes | The date and time to check theme availability for. |
