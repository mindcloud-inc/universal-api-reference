# Create One-Time Scheduling Link with NeetoCal

Creates a one-time scheduling link in NeetoCal.

## Endpoint

- **Method:** `POST`
- **Path:** `/meetings/:meeting_sid/one-off-links`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Create One-Time Scheduling Link](https://apidocs.neetocal.com/api-reference/scheduling-links/create-one-off)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
