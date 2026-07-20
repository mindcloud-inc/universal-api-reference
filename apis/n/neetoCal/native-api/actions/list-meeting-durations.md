# List Durations for a Meeting with NeetoCal

Retrieves meeting durations from NeetoCal for a scheduling link.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings/:meeting_sid/durations`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [List Durations for a Meeting](https://apidocs.neetocal.com/api-reference/meeting-durations/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
