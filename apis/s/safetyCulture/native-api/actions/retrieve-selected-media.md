# Retrieve Selected Media with SafetyCulture

Retrieves selected inspection media from SafetyCulture.

## Endpoint

- **Method:** `GET`
- **Path:** `/audits/{audit_id}/media/{media_id}`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Retrieve Selected Media](https://developer.safetyculture.com/reference/thepubservice_getinspectionmedia)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audit_id` | path | `string` | yes | The id of the inspection to retrieve media from. |
| `media_id` | path | `string` | yes | The id of the media to retrieve. |
