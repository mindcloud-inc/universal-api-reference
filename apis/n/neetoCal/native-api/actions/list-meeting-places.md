# List Places for a Meeting with NeetoCal

Retrieves meeting places from NeetoCal for a scheduling link.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings/:meeting_sid/spots`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [List Places for a Meeting](https://apidocs.neetocal.com/api-reference/meeting-places/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
