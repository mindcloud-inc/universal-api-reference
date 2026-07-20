# Retrieve Theme Within Extents with OneMap SG

Retrieves OneMap SG theme data within map extents.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/themesvc/retrieveTheme`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Retrieve Theme Within Extents](https://www.onemap.gov.sg/apidocs/themes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queryName` | query | `string` | yes | The theme query name. |
| `extents` | query | `string` | yes | The bounding box extents as four comma-separated values. |
