# Get Inspection Web Report Link with SafetyCulture

Retrieves an inspection web report link from SafetyCulture.

## Endpoint

- **Method:** `GET`
- **Path:** `/audits/{audit_id}/web_report_link`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Get Inspection Web Report Link](https://developer.safetyculture.com/reference/thepubservice_getinspectionwebreportlink)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audit_id` | path | `string` | yes | The id of the inspection to retrieve a web report link for. |
