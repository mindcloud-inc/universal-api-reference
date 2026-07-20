# Get Place with NeetoCal

Retrieves a meeting place from NeetoCal.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings/:meeting_sid/spots/:id`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Get Place](https://apidocs.neetocal.com/api-reference/meeting-places/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
| `id` | path | `string` | yes | The meeting place ID. |
