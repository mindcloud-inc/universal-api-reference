# List Available Slots with NeetoCal

Finds available slots in NeetoCal for a scheduling link.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings/:meeting_sid/slots`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [List Available Slots](https://apidocs.neetocal.com/api-reference/slots/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
| `time_zone` | query | `string` | yes | IANA time zone for slot rendering. |
| `year` | query | `string` | yes | Calendar year. |
| `month` | query | `string` | yes | Calendar month. |
| `day` | query | `string` | no | Optional calendar day. |
