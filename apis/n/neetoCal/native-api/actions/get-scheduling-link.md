# Get Scheduling Link with NeetoCal

Retrieves a scheduling link from NeetoCal.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings/:meeting_sid`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Get Scheduling Link](https://apidocs.neetocal.com/api-reference/scheduling-links/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
