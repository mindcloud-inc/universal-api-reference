# List Events with National Park Service

Retrieves events from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Events](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateEnd` | query | `string` | no | End date in yyyy-mm-dd format. |
| `dateStart` | query | `string` | no | Start date in yyyy-mm-dd format. |
| `pageNumber` | query | `string` | no | Event results page number. NPS defaults to 1. |
| `pageSize` | query | `string` | no | Number of events per page. NPS defaults to 10. |
| `parkCode` | query | `string` | no | Comma-delimited NPS park codes. |
| `q` | query | `string` | no | Search term. |
