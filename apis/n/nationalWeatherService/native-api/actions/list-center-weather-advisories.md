# List Center Weather Advisories with National Weather Service

Retrieves center weather advisories from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/aviation/cwsus/:cwsuId/cwas`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Center Weather Advisories](https://api.weather.gov/openapi.json#/paths/~1aviation~1cwsus~1{cwsuId}~1cwas/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cwsuId` | path | `string` | no | Center Weather Service Unit identifier, such as ZKC. |
