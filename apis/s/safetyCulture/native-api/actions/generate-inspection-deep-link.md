# Generate Inspection Deep Link with SafetyCulture

Generates an inspection deep link in SafetyCulture.

## Endpoint

- **Method:** `POST`
- **Path:** `/audits/{audit_id}/deep_link`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Generate Inspection Deep Link](https://developer.safetyculture.com/reference/thepubservice_getinspectiondeeplink)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audit_id` | path | `string` | yes | The id of the inspection to retrieve a deep link for. |
